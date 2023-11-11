# Super Simple Static Site Builder [s4b]

s4b is a super simple static site generator that allows you to create a
minimalist web 1.0 blog site.

## Features 

* Automatically generated archives page
* Super simple SEO: automatically generate robots.txt, RSS feed, and sitemap
* Easily upload custom style sheets
* POSIX Compliant

# Requirements 

* smu 

# Configuration

General site configurations are located in the *config* file located in the
parent directory site-builder. It is important to set the following config variables
before building!

```
URL="https://domain.tdl"  
LANG="en-us"			 
AUTHOR="John Doe"
SITETITLE="Blog Title"
KEYWORDS="list, seperated, by, commas"
DESC="What's your blog about?"

ROOT="/path/to/site-builder"

SITE="/path/to/output/dir/"
```

## Stylesheets

You can place your custom style sheets in the directory **site-builder/assets**.
Site Builder will automatically source the style sheet named **style.css**.
Other stylesheets will be ignored unless they are linked in the html head.
To add additional style sheets, you can edit the build file. 

## Images

Any images used must be placed in the **site-builder/img** directory. If you
want to source and image in your blog post, the path will be **/img/image.ext**.
If an image is not displaying correctly, make sure to to check if it is spelled
correctly and/or if the file is in the proper directory.

If you would like to set a custom favicon for your website, replace the default
**favicon.ico** file in the **site-builder/img** directory with your own. The
file type must be a .ico. 

*Tip!* Make sure to add alt-text to all your images in case they don't load
properly. Alt-text also improves SEO!

## Writing Posts

Posts must be placed in the **site-builder/posts** directory with the .md file
extension. Do **not** put .html files in this directory. The content of and
structure of the .md file can vary, however, the first line must contain a first
level heading in the form **# Title**. This first level heading will be used as
the title of your post and will appear with this title this on the archive page 
of the website.

# Running Site Builder

To run the builder, go into the parent site-builder directory and run the command:
```
./s4b 
```
This will populate the $SITE directory specified in the config file. Transfer these
files and subdirectories to your web server. 
