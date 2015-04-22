'''Linking Bootstrap to your New Rails App'''

Why use Bootstrap?

Preprocessors:
	
	Bootstrap ships with vanilla CSS, but its source code utilizes the two most popular CSS preprocessors, Less and Sass. Quickly get started with precompiled CSS or build on the source.
	
One framework, every device.

	Bootstrap easily and efficiently scales your websites and applications with a single code base, from phones to tablets to desktops with CSS media queries.
	
Full of features

	With Bootstrap, you get extensive and beautiful documentation for common HTML elements, dozens of custom HTML and CSS components, and awesome jQuery plugins.

In order to add bootstrap to your new rails app, follow the following steps:

Step 1: Add the bootstrap gem to your gemfile (gem 'bootstrap-sass')
Step 2: Goto your terminal and inside your app directory run bundle install to install the gem your just added to your app
Step 3: In your app directory goto /assets/stylesheets/application.css, right click on it and select rename file and then rename it to application.css.scss. This will add Sassy CSS to your stylesheet
Step 4: Open the application.css.scss file and add @import "bootstrap-sprockets"; @import "bootstrap"; to the end of the file
Step 5: In your app directory goto /assets/javascript/application.js, open the file and Add //= require bootstrap-sprockets above "require tree" 
Step 6: Open chrome and goto http://getbootstrap.com/getting-started/ 
Step 7: Add bootstrap CSS classes to your views
