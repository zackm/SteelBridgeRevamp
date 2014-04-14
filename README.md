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
- CSS and JS files are concatenated into single respective files for production, so please make new versions after making changes. I used the [Grunt](http://gruntjs.com/) build system to do this, so if you have [npm](https://www.npmjs.org/) and Grunt installed, then all you need to do is run '''grunt''' on the command line while in the website directory to produce these files. I also set up Grunt to do some other helpful things like compress images, take a look in the Gruntfile to see what else is set up.

### Explanation of Included Files
#### Basic Files
- '''dist/''' (folder with images, CSS, and JS for the website. This is uploaded to the OCF servers.)
- '''font/''' (folder with fonts that provide icons to use. This is also uploaded to the OCF servers.)
- '''suchwow''' (This is...something. Please keep it on the server too.)
- '''README.md''' (this file that you're reading)
- '''about.html''','''contact.html''', '''history.html''', '''index.html''', '''photos.html''', '''sponsors.html''' (These are the actual web pages. Index is the home page. Most edits will occur in these files.)

#### Advanced Files
- '''css/''' (The source SCSS files.)
- '''img/''' (The source image folder with uncompressed images.)
- '''js/''' (The source Javascript folder filled with libraries I used.)
- '''src/''' (A relic of previous directory structure, just holds the Berkeley seal with shadow .psd file.)
- '''Gruntfile.js''' (The Grunt config file)
- '''package.json''' (NPM modules required for Grunt)

### Editing Instructions
The following things should be done each year:
- Download the current version of the site. You can download this saved 2014 version of the site using the '''Download ZIP''' button to the right. However, updates may have been made to the site and not saved in github. In this case you should download the current '''public_html''' folder from the OCF servers (connection instruction below).
- -
- update history to include past year
- add more photos albums (flickr, get credentials from past webmaster/PM)
- update contact info & officers
- if desired, update slideshow on homepage

### Uploading Instructions
- The site is hosted on Berkeley's [OCF](http://ocf.berkeley.edu) servers.
- Set up a SFTP (ssh file transfer protocol) into OCF. The easiest way to do this is to download [Cyberduck](http://cyberduck.io/) or a similar program and create a new STFP connection with the following settings: Host Name: ssh.ocf.berkeley.edu, Port: 22. Get the username and password from the last web maintainer (below) or the previous PM. Once connected, you will see a set of folders. This is where the site files are placed.
- Specifically, the website files are put into the '''public_html''' folder. You should copy the '''dist''' and ''font''' folders and all .html files into this folder. After updating these files, the live website should update also.
- [OCF Connection Instructions](http://wiki.ocf.berkeley.edu/services/shell/)

### Contact Instructions
- last website maintainer: Zack Mayeda (Fall 2013, Spring 2014)
