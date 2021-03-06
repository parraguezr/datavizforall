# Fix Common GitHub and Code Errors
*By [Jack Dougherty](../../introduction/who.md), last updated March 25, 2017*

What happens if you cannot view your published GitHub repository, or if your code breaks and no longer displays what it was designed to show? These are common problems, especially for newer students, because accidentally clicking the wrong box or mistakenly erasing a single character (such as a semicolon) can make your visualization seem to vanish, even though your work is usually still there. Breaking your code -- and figuring out how to fix it -- is a great way to learn, even if it requires trial and error.

## Safely Delete your GitHub Repo and Start Over
If you need to delete your GitHub repo and start over, here's a simple way to safely save your work:
- Go to the top-level of your GitHub repository, similar to ```https://github.com/USERNAME/REPOSITORY```
- Click the green "Clone or Download" button, and select Download Zip to receive a compressed folder of your repo contents on your computer.
- In your GitHub repo, click on Settings (upper-right area) and scroll down to Delete This Repository.
- To prevent accidental deletions, GitHub requires you to type in the REPOSITORY name.
- Now you can start over in one of these ways:
  - If you wish to [Create a Simple Web Page with GitHub Pages](../../embed/github-pages), follow that tutorial again.
  - OR
  - Fork another copy of the original GitHub repository to your account. After you create your copy, if you wish to add selected files that you previously downloaded to your computer, follow directions to [Upload Code with GitHub](../create-repo) in the second half of this tutorial in this book

## Problems with Creating a Simple Web Page with GitHub Pages
If you followed the [Create a Simple Web Page with GitHub Pages tutorial](../../embed/github-pages), it should have created two web links (or URLs):
- your code repository, in this format: ```https://github.com/USERNAME/REPOSITORY```
- your published web page, in this format: ```https://USERNAME.github.io/REPOSITORY```

Be sure to insert your GitHub username, and your GitHub repository name, in the general formats above.

These URLs are NOT case-sensitive, which means that ```https://github.com/USERNAME``` and ```https://gitub.com/username``` point to the same location.

#### My simple GitHub web page does not appear
- Make sure that you are pointing to the correct URL for your published web page, in the format shown above.
- Be patient. During busy periods on GitHub, it may take up to 1 minute for new content to appear in your browser.
- Do a "hard refresh" to [bypass any saved content in your browser cache](https://en.wikipedia.org/wiki/Wikipedia:Bypass_your_cache).
  - Ctrl + F5 (most Windows-Linux browsers)
  - Command + Shift + R (Chrome or Firefox for Mac)
  - Shift + Reload button toolbar (Safari for Mac)
- Test the link to your published web page in a different browser. If you normally use Chrome, try Firefox.
- On rare occasions, the GitHub service or GitHub Pages feature may be down. Check https://status.github.com/

#### My simple GitHub web page does not display my iFrame  
- If you followed the [Create a Simple Web Page with GitHub Pages tutorial](../../embed/github-pages) and inserted an iframe in the README.md file, it will appear in your published web page, under these conditions:
  - Ideally, your README.md should be the ONLY file in this GitHub repository
  - Any other files in your repo (such as index.html, default.html, or index.md) will block the iFrame HTML code in your README.md from being published on the web. If you accidentally selected a GitHub Pages Theme, you need to delete any extra files it created: click each file, select trash can to delete it, and commit changes.

![Screenshot: Extra files in GitHub repo will block iFrame in your README](extra-files-block-readme-iframe.png)

## Problems with iFrames

#### My iFrame does not appear in my web page
- Go back to the [Embed tutorials in this book](../../embed) to double-check the directions
- Items listed in your iFrame (such as the URL, width, or height) should be enclosed inside straight quotation marks (single or double)
  - BROKEN iFrame (missing quotation marks for width and height)
  ```
  <iframe src="https://jackdougherty.github.io/leaflet-map-simple" width=90% height=350></iframe>
  ```
  - FIXED iFrame (with correct quotation marks)
  ```
  <iframe src="https://jackdougherty.github.io/leaflet-map-simple" width="90%" height="350"></iframe>
  ```
- Use only ```https``` (the extra 's' means 'secure'), not ```http```. Some web browsers will block content if it mixes http and https resources, and some code templates in this book require https.

![Screenshot: Replace http with https](http-vs-https.png)

- Use only straight quotes, not curly quotes. Avoid pasting text from a word-processor into GitHub, which can accidentally carry over curly quotes. Typing directly into the GitHub editor will create straight quotes.

![Screenshot: Curly quotes versus straight quotes](curly-vs-straight-quotes.png)

## Problems with Leaflet Maps with Google Sheets template

#### My map does not appear
1) Confirm that you have completed all of the key steps in the [Leaflet Maps with Google Sheets](../../leaflet/with-google-sheets) tutorial in this book, especially these:
  - Sign in to Google and File > Make a Copy of the Google Sheet to your Google Drive.
  - File > Publish your Google Sheet (Jack often forgets this key step!)
  - Copy your Google Sheet web address from top of your browser (usually ends with ```...XYZ/edit#gid=0```) and paste into your ```google-doc-url.js``` file in your GitHub repo. Do NOT copy the *Published* web address (which usually ends with ```...XYZ/pubhtml```)
  - When you paste your Google Sheet web address into ```google-doc-url.js```, be careful not to erase single-quote marks or semicolon
  - Go to your live map link, which should follow this format: ```https://USERNAME.github.io/REPOSITORY```, refresh the browser, and wait at least 30 seconds.

2) Check your Google Sheet for errors:
- Do NOT rename column headers (in row 1) of any sheet, because the Leaflet Map code looks for these exact words.

![Screenshot: User accidentally renamed column headers in the Points tab](lmwgs-fix-column-headers.png)

- Do NOT rename row labels (in column A) of any sheet, due to the same reason above.

![Screenshot: Do not rename or delete](lmwgs-do-not-rename-lables.png)

- In your Points tab, DO NOT leave any blank rows

3) Confirm on GitHub Status (https://status.github.com/) that all systems are operational.

4) If you cannot find the problem, go to the top of this page to Safely Delete Your GitHub Repo and Start Over. Also, make a new copy of the Google Sheet template, give it a new name, and copy data from your old sheet using File > Paste Special > Values Only.

## Problems with Highcharts code templates

#### Chart displays old data
If you upload new data to your Highcharts code template on GitHub Pages, and it does not appear in your browser after refreshing and waiting up to one minute, then GitHub Pages is probably not the cause of the problem. Instead, some browsers continue to show "old" Highcharts in the web cache. The simplest solution is to File > Quit your browser and re-open the link to your Highcharts.

## Problems with Mac Computers

#### No file extensions

Several tools in this book will not work properly if your Mac Finder does not display file extensions. In other words, every file should include a period followed by several letters (such as data.csv and map.geojson). If you do not see these extensions at the end of each file name, then go to Finder > Preferences > Advanced and check the box to turn them on, as show below:

![Screenshot: Checkbox to show filename extensions](mac-finder-filename-extensions.png)

## Solve Problems with Browser Developer Tools
Peek inside any website and view the web code under the hood with the browser developer tools.

In Chrome for Mac, go to View > Developer > Developer Tools

![](Chrome-developer-tools.png)

In Firefox for Mac, go to Tools > Web Developer > Inspector

![](Firefox-tools-inspector.png)


{% footer %}
{% endfooter %}
