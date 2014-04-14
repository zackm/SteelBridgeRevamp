The Official Website of UC Berkeley's Steel Bridge Team
=================

### Getting Started
Are you thinking about maintaining the steel bridge team's website? Here are the skills required to make changes to this site:
- Ability to use a text editor like Sublime Text, TextMate, TextEdit, Emacs, or Notepad++...
- Knowledge of HTML if helpful, but definitely not required. Most editing is just duplicating existing code or replacing contact info from year to year.
- Basic image editing (resizing, cropping, uploading to flickr)
- Ability to use an FTP client (like Cyberduck or Transmit)
- Ability to email the previous webmaster if everything goes horribly wrong

### Site Overview
- This is a static site, so to make changes you must edit the source HTML files and re-upload them to the OCF servers (more info on this below).
- Images on the photos page are saved on Flickr. A new Flickr set should be made for each year.
> Knowledgeable web developers can keep reading, but the following info isn't critical to make yearly updates to the site.
- Styling is done with [SASS](http://sass-lang.com/). You can write with normal CSS syntax in .scss files, but then you have to compile it into a .css file before using the styles on the production site. All source css files are in the '''css''' folder. The compiled, production ready CSS is in '''dist/prod.css'''.
- CSS and JS files are concatenated into single respective files for production, so please make new versions after making changes. I used the [Grunt](http://gruntjs.com/) build system to do this, so if you have [npm](https://www.npmjs.org/) and Grunt installed, then all you need to do is run '''grunt''' on the command line while in the website directory to produce these files.

### Explanation of Included Files
#### Basic Files
- dist/ (folder with HTML, CSS, and JS for the website. this is uploaded to the OCF servers)
- src/ (uncompiled source code for all CSS and JS. for pros only)
- README.md (this file)
#### Advanced Files
- '''Gruntfile.js'''

### Editing Instructions
The following things should be done each year:
- update history to include past year
- add more photos albums (flickr, get credentials from past webmaster/PM)
- update contact info & officers
- if desired, update slideshow on homepage

### Uploading Instructions
- hosted on Berkeley's OCF
- FTP into OCF
- transfer files into public_html folder
- (link to their instructions)
- you can download this version of the site, or contact me to get edit privileges to this repo

### Contact Instructions
- last website maintainer: Zack Mayeda (Fall 2013, Spring 2014)
