# Slides for W3C Offices

This presentation uses the HTML5-based [shower.js](https://github.com/shower/shower "Shower.JS Library") engine.

## How to use it

The easiest way: download the [full package as a ZIP](https://github.com/espinr/join-w3c-slides/archive/master.zip) file and extract its content where you want to deploy the presentation. Change the name of the root folder (e.g., `w3c-slides`).   

This package contains all the basic files needed to perform the presentation. 
- `lib` -> library
- `img` -> images
- `video` -> videos 
- `index.html` -> Main document with the slides content

Both `img` and `video` are the directories to store multimedia resources. They included only the elements needed for the basic presentation.

`index.html` is the HTML document containing the presentation. Here you can change content and styles. 

### Structure of presentation

The `index.html` file has the following structure:

	<!DOCTYPE html>
	<html lang="en">
	<head>
		<title>Join World Wide Web Consortium</title>
		[…]
		<link rel="stylesheet" href="./lib/shower/themes/w3c/styles/screen-16x10.css">

By specifying the css file, you can set up the ratio of the screen: either 16x10 or 4x3. To use 4x3 proportion, just change css to:

		<link rel="stylesheet" href="./lib/shower/themes/w3c/styles/screen-4x3.css">

The next section is styles, were you can customize visualization of slides. 

		<style>
			.slide p { line-height: 1.5em; }
			[…]

In the body of the document you will find a `header` with the main title and subtitle of the presentation.

	<header class="caption">
		<h1>your title</h1>
		<p>your subtitle</p>
	</header>

Slides have this structure:

	<section class="slide"> 	<!-- always include .slide -->
		<h2>title of slide</h2>
		<p>any HTML element such as paragraphs</p>
		<ul>
			<li>lists</li>
		</ul>
		<blockquote>blockquotes, etc.</blockquote>
		<!-- Whatever you need -->
	</section>

The cover slide will be identified as `cover`

	<section class="slide" id="cover">
		<h2>…</h2>
		<p>…</p>
	</section>


## Theme

Look and feel of slides can be adapted. You can change the basic theme, or building a new one. In order to customize the basic template, just copy one of the existing folders in `lib/shower/themes/` and tweak css files in the `styles` folder.

You can change the ribbon image that is shown on the presentation. Just change `/w3c/images/ribbon.svg`.

