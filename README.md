JavaScript Plugin Starter
===

This is my starter structure for a generic *JavaScript plugin*. It makes use of several technologies as described below.

###Use:
In every file you'll see a piece of commented code. That's the instructions for each file. In others you'll see *UPPERCASED-WORDS* and those one you should change to fit your needs like the name of the plugin, version, your GitHub user, the repository URL and so. 

Files should be new names too (*your-javascript-plugin-name.js*) and they're commanded in `Gruntfile.js` so change names there there too, it's clearly identified.

demo
--
Folder that holds the demo for this plugin. The basic files are:

- **index.html**: the demo page
- **css/style.css**: gives CSS styles to the demo page. Now it is a plain .css but you can add your pre-processor of choice.
- **images**: If you need add images to your demo, otherwise just delete this folder.
- **js/**: In case you need libraries/plugins you should add them here (for example, jquery.min.js), otherwise just delete this folder.

dist
--
Files that are ready for production, minified and packed versions. The minified one is called directly from `demo/index.html`.

- **your-javascript-plugin-name.js** *(&#9888; rename this)*
- **your-javascript-plugin-name.min.js** *(&#9888; rename this)*

src
--
Your plugin as you code it. Then this file will be added to a workflow and prepared for production.

- **your-javascript-plugin-name.js** *(&#9888; rename this)*

your-javascript-plugin-name.json
--
This JSON file holds many configuration texts, basically to identify your plugin and generate the final files.

*(&#9888; rename this and look inside)*

Gruntfile.js
--

File that commands **GruntJS** tasks and take care of several behaviors:

- **meta**: add a commented piece of text in the top of the generated JS files.
- **concat**: combine JS files. *(&#9888; change name here)*
- **jshint**: looks for improvements in the JS code. *(&#9888; hange name here)*
- **uglify**: minify code to a **.min.js** file. *(&#9888; change name here)*
- **watch**: using [Livereload](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei) watch for changes in HTML/JS files and reload the browser if there is any.

There are 2 main tasks:

> **default**: concats and minifies the file, from `/src` to `/dist`.

*Use*:
	
	$ grunt
	
or:

	$ grunt watch
	
> **testjs**: very helpful, run this one everytime you think you have a working demo. It looks for errors and improvements in your JavaScript code and shows suggestions.

*Use*:
	
	$ grunt testjs


package.json
--

Take care of the **NodeJS** packages needed by **GruntJS**, as decribed before. You can install them using: 

	$ npm install

and if you need more (for example a CSS pre-processor to write your demo) just add them using:
	
	 $ npm install grunt-libraryname --save-dev

The basic ones are:

- grunt
- grunt-cli
- grunt-contrib-concat
- grunt-contrib-jshint
- grunt-contrib-uglify
- grunt-contrib-watch

README.MD
--

This file, you should overwrite it and document your own plugin.

LICENSE
--

I use [MIT](http://opensource.org/licenses/MIT) by default, but it's up to you. Any piece of working code should have a license. [Choose one](http://en.wikipedia.org/wiki/Comparison_of_free_and_open-source_software_licenses#General_comparison).

