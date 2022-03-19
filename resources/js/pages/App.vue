<template>
  <div class="container p-3" style="max-width: 500px">
    <header>
      <div class="p-3 pb-md-4 mx-auto text-center">
        <h1 class="display-4 fw-normal">Todo List</h1>
      </div>
    </header>

    <main>
      <div class="card bg-light">
        <article class="card-body mx-auto w-100" style="max-width: 350px">
          <h4 class="card-title mt-3 text-center">Add a task</h4>

          <div class="mb-3 input-group">
            <add v-on:reloadList="getItemsFromDB()" />
          </div>
        </article>
      </div>

      <div class="card bg-light">
        <article class="card-body mx-auto w-100" style="max-width: 350px">
          <!-- In larger applications, these events are usually controlled with
          the state -->
          <index :items="items" v-on:reloadList="getItemsFromDB()" />
        </article>
      </div>
    </main>
    <!-- :items attaches the obtained items from the DB to a prop of the Index component -->
  </div>
</template>

<script>
import Add from "./items/Add.vue";
import Index from "./items/Index.vue";

export default {
  components: {
    Add,
    Index,
  },
  data: function () {
    return {
      items: [],
    };
  },
  methods: {
    getItemsFromDB() {
      axios
        .get("/api/items")
        .then((response) => {
          this.items = response.data;
          this.items.forEach((item) => {
            item.completed = item.completed ? true : false;
          });
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
  created() {
    this.getItemsFromDB();
  },
};
</script>