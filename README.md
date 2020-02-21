# CakesBySaray.com - Static Site

This is the repo for the cakesbysaray.com static site. This site does not have any automation built in, no build scripts, nothing like that. Instead _you_ have to do a bit more work. Below is the process I took to update the site.

### Update process

- __Clone this repo to your machine__
	```
	git clone https://github.com/MoticorpIT/cakesbysaray
	```
- __Make changes to the site__

	If you're changes involve css or js, be aware that the html file links to minified versions, so your changes may not show by default. __DO NOT REMOVE THE MINIFIED VERSIONS__ from the html links. This is done to help performance, and this site needs all the help it can get.

- __Minify files__ (as needed)

	If your changes involved changes to what is a minified css file or javascript file on the server, you will need to minify the revised file. I used [Minifier.org](https://www.minifier.org/). You'll need to copy your files contents into the field on the Minifier website. Make sure you have the correct language selected (css or js) and click minify. Copy and paste the resulting code into the minified version of the file.

	__Minification Example__
	1. Copy contents from `styles.css`
	2. Paste code into the Minifier website, choose css, click minifiy and copy the resulting code
	3. Paste the resulting code into `styles.min.css`
	4. Repeat the same process, substituting file names with the files needing to be reminified.

- __Copy updated files to the server__
	1. Log onto the cakesbysaray server via an FTP client
	2. Navigate to the `public_html` directory
	3. Replace the updated files
		- If you're thinking of using the folder sync feature of your FTP client, it isn't recommended, but if you do it anyway, do so with extreme caution and don't come to me when its broke. This site doesn't take long to backup, might be worth it. 

- __Check live site__
Before you call it good, varify your changes have been applied, but more importantly _**make sure the site still appears and functions as it did before you made updates**_
