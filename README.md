The Official Website of UC Berkeley's Steel Bridge Team

### Getting Started

> Are you thinking about maintaining the steel bridge team's website? Here are the skills required to make changes to this site:

- Ability to use a text editor like Sublime Text, TextMate, TextEdit, Emacs, or Notepad++...
- Knowledge of HTML if helpful, but definitely not required. Most editing is just duplicating existing code or replacing contact info from year to year.
- Basic image editing (resizing, cropping, uploading to flickr)
- Ability to use an FTP client (like Cyberduck or Transmit)
- Ability to email the previous webmaster if everything goes horribly wrong

### Site Overview
- This is a static site, so to make changes you must edit the source HTML files and re-upload them to the OCF servers (more info on this below).
- Images on the photos page are saved on Flickr. A new Flickr set should be made for each year.

> Knowledgeable web developers can keep reading, but the following info isn't critical to make yearly updates to the site.

- Styling is done with [SASS](http://sass-lang.com/). You can write with normal CSS syntax in .scss files, but then you have to compile it into a .css file before using the styles on the production site. All source css files are in the ```css``` folder. The compiled, production ready CSS is in ```dist/prod.css```.
- CSS and JS files are concatenated into single respective files for production, so please make new versions after making changes. I used the [Grunt](http://gruntjs.com/) build system to do this, so if you have [npm](https://www.npmjs.org/) and Grunt installed, then all you need to do is run '''grunt''' on the command line while in the website directory to produce these files. I also set up Grunt to do some other helpful things like compress images, take a look in the Gruntfile to see what else is set up.
- Most website files are stored on Github, [here](https://github.com/zackm/SteelBridgeRevamp). A development version of the site is automatically hosted on github when you push to the ```gh-pages``` branch of this repo. To read up on github pages, read [here](https://pages.github.com/). To see the version of the website hosted on github, click [here](http://zackm.github.io/SteelBridgeRevamp/);

### Explanation of Included Files
#### Basic Files
- ```dist/``` (folder with images, CSS, and JS for the website. This is uploaded to the OCF servers.)
- ```font/``` (folder with fonts that provide icons to use. This is also uploaded to the OCF servers.)
- ```suchwow``` (This is...something. Please keep it on the server too.)
- ```README.md``` (this file that you're reading)
- ```about.html```,```contact.html```, ```history.html```, ```index.html```, ```photos.html```, ```sponsors.html``` (These are the actual web pages. Index is the home page. Most edits will occur in these files.)

#### Advanced Files
- ```src/``` (A relic of previous directory structure, just holds the Berkeley seal with shadow .psd file.)
  - ```css/``` (The source SCSS files.)
  - ```img/``` (The source image folder with uncompressed images.)
  - ```js/``` (The source Javascript folder filled with libraries I used.)
- ```Gruntfile.js``` (The Grunt config file)
- ```package.json``` (NPM modules required for Grunt)

### Editing Instructions
The following things should be done each year:
- Download the current version of the site. You can download this saved 2014 version of the site using the ```Download ZIP``` button to the right. However, the site may have been updated and not saved in github. In this case you should download the current ```public_html``` folder from the OCF servers (connection instructions below).
I'll walk through the changes that are needed for each page on the site. I've also included helpful notes in the html files themselves. Lines that look like this ```<!-- Hello! -->``` are comments and don't show up on the site.
- Home page (index.html)
  - No mandatory changes on this page, just fun ones :)
  - You can add/alter/remove photos in the photo slider. Photos that are added must be 1450px x 500px and should be put in the ```dist/img/slider/``` folder.
  - Add the correct html for each photo (documented in html file), and add an indicator for each new photo. Indicators are the dots below the photos that let you skip to certain photos. Make sure to have the same number of indicators in the html as you have photos.
- About page
  - No mandatory changes on this page. Feel free to alter the text though. Pictures too.
- History page
  - Add the results from the previous year! (Hopefully things went well)
  - Copy an existing 'history item' html block (denoted in html file) and paste it at the top of the list (correct location also denoted in html file). Alter the team name, year, PM, press links, photo, and t-shirt logo. The t-shirt image should be a 90px x 90px photo in the ```dist/img/icons/``` folder. The photo for the year should be a really nice photo and should be at least 500px x 450px. It's ok if it's not those exact dimensions.
- Photos page
  - Just do your best here, I understand flickr can be annoying to work with.
  - We host photos on flickr, so you'll need to get the flickr login from the PM or previous webmaster. The flickr username is calsteelbridge. Albums can be viewed [here](https://www.flickr.com/photos/115191193@N02/sets/).
  - Here are flickr uploading instructions as of April 2014: 
    - Click upload and select photos for the past year.
    - Add them to a new public album called "UC Berkeley Steel Bridge 20XX"
    - After creating the album, view the album and note the url. There should be a long number at the end, like ```/sets/3484583495034/```. Copy that number.
  - Now that you've uploaded the photos to flickr, open up the html file for our site.
  - Duplicate a "gallery item" as denoted in the file and change the year. Also change the ID where marked. The new ID should match the year of the album you're adding. The actual gallery is created with javascript, so all you'll see in the html file is ```<div id='gallery-2014'></div>```.
  - Go to the bottom of the file and edit the javascript to know to insert a new gallery. Find the area where there are a bunch of lines with ```Galleria.run..```. Copy and paste the marked line. Edit the copy to have the same ID that you just created and replace the long number with the album number that you copied from the url earlier.
  - Give it a try and make sure it works!
- Sponsors page
  - No mandatory changes on this page.
  - If you want to add a sponsor, get the sponsor's logo and make it black and white with photoshop or another photo editor. Save the image as a png and make sure it is as most 350px x 350px. It's ok if it's not that exact size, most existing logos are 350px x 140px. Put the image in the ```dist/img/sponsors/``` file.
  - If there are fewer than 3 logos on the bottom row, follow the instructions in the html to insert the new logo. All that is required is to edit an img source, and add a div.
  - If the bottom row of logos is full with 3 images already, you'll need to duplicate a whole row's html. Copy the denoted html block and paste it to the bottom of the page.
- Contact page
  - You're almost done! Now you just need to update the PM's info.
  - Replace the PM name and email where noted in the html.
- That's it! :sparkles: Congratulations! :sparkles: Now upload it to the OCF servers! Instructions below:
- Now add yourself to the list of website maintainers at the bottom of this file. Don't worry about adding your email if you're not comfortable with that. Just make sure the PM's email is on the site, and then questions can go through them.

### Contact Instructions
- last website maintainer: Zack Mayeda (Fall 2013, Spring 2014)

