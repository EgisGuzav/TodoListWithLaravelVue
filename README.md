<div id="top"></div>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">TodoListWithtLaravelVue</h3>

  <p align="center">
    A basic project to know how to use Vue 3 along with Laravel 9.
    <br />
    <a href="https://github.com/HenestrosaConH/TodoListWithtLaravelVue/issues">Report Bug</a>
    ·
    <a href="https://github.com/HenestrosaConH/TodoListWithtLaravelVue/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
    </li>
		<li>
			<a href="#setting-up-vue-3-and-bootstrap-5">Setting up Vue 3 and Bootstrap 5</a>
			<ul>
				<li><a href="#installation-of-vue-3">Installation of Vue 3</a></li>
				<li><a href="#setting-up-vue-3-in-the-project">Setting up Vue 3 in the project</a></li>
				<li><a href="#installation-of-bootstrap-5">Installation of Boostrap 5</a></li>
				<li><a href="#setting-up-bootstrap-5-in-the-project">Setting up Boostrap 5 in the project</a></li>
			</ul>
		</li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

<p>
	As the description of the repository says, this is a small project that I've made following the basic structure of
	<a href="https://www.youtube.com/watch?app=desktop&v=UHSipe7pSac&ab_channel=Scrypster">this video</a> by the Youtube user
	<a href="https://www.youtube.com/channel/UCR1_G0EoEIb87wi3GPlk-CQ">Scrypster</a>.
</p>

<p>
	The original creator makes the application in Vue 2 and Laravel 8, whereas I've made it in Vue 3 and Laravel 9.
	I've also made use of Bootstrap 5 to give some basic yet elegant style to the elements.
</p>

<p>
	There are some changes that I consider as an improvement over the original project (aside from the design), 
	such as the following:
	<ul> 
		<li>Checking the checkbox if the task has already been completed when getting the items through the API.</li> 
		<li>
			Including translations declared in the files located in the 'lang' folder. This has been possible thanks to the
			<a href="https://github.com/kg-bot/laravel-localization-to-vue">Laravel localization to Vue</a> 
			package.
		</li>
		<li>
			Cleaner organization of the <code>resources/js</code> directory along with renaming many of the <code>.js</code> and <code>.vue</code> files to ensure a cohesive and simple structure.
		</li>
	</ul>
</p>

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- BUILT WITH -->

### Built With

-   [Vue 3](https://vuejs.org/)
-   [Laravel 9](https://laravel.com)
-   [Bootstrap 5](https://getbootstrap.com)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

To make the project work on your PC, you have to create a <code>.env</code> file and specify there the 
credentials of the DB that you'll have to create in order to make CRUD operations with the tasks.

You'll have to execute <code>composer install</code> and <code>npm install</code> to install the packages indicated in the files <code>composer.lock</code> and <code>package-lock.json</code>, respectively.


Don't forget to use Apache Server (or such as the likes of it) to host the application (I like to use Laragon in Windows and Valet in Mac for local deployment) and to run the <code>npm run watch</code> command to auto-compile the changes that you apply in the project.

<!-- SETTING UP VUE 3 AND BOOTSTRAP 5 -->

## Setting up Vue 3 and Bootstrap 5

Even though these frameworks are included in the project right off the bat, I'll show you how to get Vue 3 and Bootstrap 5 working on Laravel 9 from the beginning.

<!-- INSTALLATION OF VUE 3 -->
### Installation of Vue 3

<ol>
	<li>
		We need to install npm in our project by executing <code>npm install</code> in the root of it
	</li>
	<li>
		Once npm has been installed, we need to install the Vue package by executing <code>npm install vue ^3.0.0</code>.
	</li>
</ol>

<!-- SETTING UP VUE 3 IN THE PROJECT -->
### Setting up Vue 3 in the project

Now that Vue has been downloaded into the project, we need to add <code>.vue()</code> to <code>mix.js("resources/js/app.js", "public/js")</code> in the <code>webpack.mix.js</code> file in order to pass options to configure global styles and Vue component style extraction in Laravel.

<hr>

<!-- INSTALLATION OF BOOTSTRAP 5 -->
### Installation of Bootstrap 5

<ol>
	<li>
		In case that you haven't downloaded npm yet, you'll have to execute <code>npm install</code> in the root of the project.
	</li>
	<li>
		Once npm has been installed, we need to install Bootstrap by executing <code>npm install bootstrap</code>.
	</li>
	<li>
		We'll also have to install SASS and SASS loader in our project because Bootstrap makes use of this preprocessor of CSS. We do it by executing <code>npm install sass</code>.
	</li>
	<li>
		Once the installation has finished, we need to install the SASS processor to convert the SASS code to CSS. The command is <code>npm install sass-loader</code>.
	</li>
</ol>

<!-- SETTING UP BOOTSTRAP 5 IN THE PROJECT -->
### Setting up Bootstrap 5 in the project

<ol>
	<li>
		<p>
			In case that <code>resources/sass/app.scss</code> is not present in the project, we need to create the <code>sass</code>
			directory inside the <code>resources</code> directory. Then, we'll create the <code>app.css</code> file in order to add
			the line <code>@import '~bootstrap';</code>. 
		</p>
		<p>
		  By the way, just a thought aside: the <code>bootstraping</code> directory of the root of any Laravel project has nothing to do with the CSS library. As the Stackoverflow user <a href="https://stackoverflow.com/users/205528/kien-truong">kien-truong</a> points out on <a href="https://stackoverflow.com/a/23902038/15675885">this answer</a>, it's used to initialize (setting up path and environments) the framework. 
		</p>
	</li>
	<li>
		Having done that, now we have to append <code>.sass('resources/sass/app.scss', 'public/css')</code> to the <code>mix</code> to let Laravel know that the compiled version of the SASS styles have to be moved into the <code>public/css</code> directory.
	</li>
	<li>Now we can compile the project to generate the CSS file in the <code>public/css</code> directory that we just set up by executing <code>npm run dev</code>.</li>
	<li>
		If you have followed all the steps correctly, now you only have to add <code>&lt;link href="{{ asset('css/app.css') }}" rel="stylesheet"&gt;</code> (or <code>mix('css/app.css')</code>, depending of your purpose) to the <code>&lt;head&gt;</code> of the Blade templates to import the stylesheet generated by Webpack.</li>
</ol>

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Original Creator: [Scrypster](https://www.youtube.com/channel/UCR1_G0EoEIb87wi3GPlk-CQ)

Author of this repository: henestrosaconh@gmail.com - [LinkedIn](https://www.linkedin.com/in/josecarloslh/)

Project Link: [https://github.com/HenestrosaConH/TodoListWithtLaravelVue](https://github.com/HenestrosaConH/TodoListWithtLaravelVue)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

As I said at the beginning, all the credits to <a href="https://www.youtube.com/channel/UCR1_G0EoEIb87wi3GPlk-CQ">Scrypster</a> for
the initial idea of the project and to these repositories that have helped me to make this project/README:

-   [Laravel localization to Vue](https://github.com/kg-bot/laravel-localization-to-vue)
-   [FontAwesome](https://fontawesome.com/docs/web/use-with/vue/)
-   [Best-README-Template](https://github.com/othneildrew/Best-README-Template/)
-   [Img Shields](https://shields.io)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/HenestrosaConH/TodoListWithtLaravelVue.svg?style=for-the-badge
[contributors-url]: https://github.com/HenestrosaConH/TodoListWithtLaravelVue/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/HenestrosaConH/TodoListWithtLaravelVue.svg?style=for-the-badge
[forks-url]: https://github.com/HenestrosaConH/TodoListWithtLaravelVue/network/members
[stars-shield]: https://img.shields.io/github/stars/HenestrosaConH/TodoListWithtLaravelVue.svg?style=for-the-badge
[stars-url]: https://github.com/HenestrosaConH/TodoListWithtLaravelVue/stargazers
[issues-shield]: https://img.shields.io/github/issues/HenestrosaConH/TodoListWithtLaravelVue.svg?style=for-the-badge
[issues-url]: https://github.com/HenestrosaConH/TodoListWithtLaravelVue/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/henestrosaconh
[product-screenshot]: screenshots/screenshot.png
