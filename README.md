# UCL Learning Analytics & Technology Lab website

A quick way for everyone to learn how to use GitHub and Markdown. (Site design 
based on [al-folio](https://github.com/alshedivat/al-folio).)

## The super-basics
Hopefully, everyone in the lab will be able to:
- [Update their own "team" profile](#how-to-update-or-add-a-team-profile)
- [Update the list of publications](#how-to-update-the-publication-list)
- [Add news posts](#how-to-add-news-posts)

To do this, you'll first need to understand a little about: 
1. **GitHub**. For our purposes, you can think of GitHub as being like 
supercharged Google Docs for code. Multiple people can work on the same code, it 
keeps track of who made what changes and when, it's easy to reverse changes that 
have been made, and different versions can be developed at the same time. One 
nice feature for our site: instead of directly editing in HTML (which is not a 
language really meant for humans to understand), you'll be giving GitHub 
information in two human-readable formats, which a GitHub tool called Jekyll 
will use to generate the HTML. 
2. **Markdown**. This README.md file is written in Markdown. Markdown allows 
for simple formatting like **bold** (double asterisks like this: `**bold**`), 
*italics* (single asterisks like this: `*italics*`), and 
[hyperlinks](http://www.ucl.ac.uk) (put the linked text in square brackets 
immediately followed by the address in parens, like: 
`[hyperlinks](http://www.ucl.ac.uk)`). See 
[this cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) 
for more details; you can also check out the markdown in this README file by 
opening 
[uclat-lab.github.io/README.md](https://github.com/uclat-lab/uclat-lab.github.io/blob/master/README.md) 
and clicking "Raw."
3. **YAML**. YAML is a structured data format that uses space-indents 
(no tab-indents!) to show structure and uses colons to associate fields with 
values. For example:
    ```
    - name: 
      position: 
      email: 
    - name: 
      position: 
      email: 
    ```
    This list has three entries. Each entry has fields for name, position, and 
    e-mail address. Note that you don't have to put strings within quotation 
    marks, although sometimes this is helpful if your string has special 
    characters like colons or quotation marks. You can also often embed Markdown 
    code like asterisks in these strings. 
    
## How to update (or add) a team profile
Two steps:
### 1. If you don't have one yet, add a picture to /assets/img/
A good size for team member pictures on this site is 311 pixels wide, in jpeg or 
png format. Name your picture file something descriptive that won't be mistaken 
for any other image on the site (like `team_your-name.jpg` -- underscores to 
separate kinds of info and hyphens to break up words). Navigate to 
[/assets/img/](https://github.com/uclat-lab/uclat-lab.github.io/tree/master/assets/img) 
and drag-and-drop the picture file from your desktop into the browser window. 
You'll then be asked to make a "commit":

![Screenshot-commit-image](assets/img/site_readme-02-commit-image.png)

In the box below **Commit changes**, instead of "Add files via upload" type in a 
more informative description like "upload `YOUR FILENAME` for members.yml" and 
click the green button to commit the file directly to the master branch.

### 2. Edit the team member data in the YAML file /_data/members.yml
Navigate to [/_data/members.yml](https://github.com/uclat-lab/uclat-lab.github.io/blob/master/_data/members.yml) 
and click the pencil for "Edit this file":

![Screenshot-edit-members](assets/img/site_readme-01-edit-data-members.png)

If you already have a profile, you'll see fields for your name, degrees, 
position, e-mail address and so forth. E.g.:

```
- name: 
  image: 
  altimage: 
  position: 
  email: 
  scholar: 
  twitter: 
  description: 
```
If you don't yet have a profile, you'll need to create a new one roughly 
matching the format of the existing entries. 

At the bottom of the page you'll see another **Commit changes** box. In the box 
below, you can write something like "Update members.yml to include `YOUR NAME`" 
and click the green button to commit the file directly to the master branch. 

After you commit, it might take a minute or two to see these changes reflected 
in the "team" page, and you might need to refresh your browser. 

## How to update the publication list

For journal articles and reviews: no book chapters, letters to the editor, 
conference abstracts, etc.

### 1. Get citation 

### 2. Find a publication image and upload

### 3. Edit the publication data in /_data/publications.yml
Use the same methods described above *(2. Edit the team member data in the YAML 
file /_data/members.yml)* to edit 
[publications.yml](https://github.com/uclat-lab/uclat-lab.github.io/blob/master/_data/publications.yml). 
This list contains publications in reverse chronological order, try to put the 
new article in the right place. Use the Vancouver-formatted text file that you 
downloaded to your computer to fill out these data entries, roughly matching the 
format of the existing entries, e.g.:
```
- authors: 
  title: 
  details: 
  year: 
  image: 
```
In `authors: ` use double asterisks (`**Name**`) to highlight lab members' 
names. For consistency, keep the final period `.` at the end of the string for 
`authors: `, `title: ` and `details: `, and change the title to 
[sentence case](https://en.wikipedia.org/wiki/Letter_case#Sentence_case) if 
necessary. Also under `details: `, spell out the actual journal title but leave 
out "The" at the beginning of journal 
titles, e.g. "~~The~~ Journal of XYZ." After `image: `, enter the name of the 
publication image you uploaded to 
[/assets/img/](https://github.com/uclat-lab/uclat-lab.github.io/tree/master/assets/img) 
in the previous step. 

**Commit changes** when you're done, using the green button to commit the file directly to the master branch and the description box below to leave a brief description. 


## How to add news posts
For this you will create a Markdown file containing the news post. Navigate to 
[/_posts/](https://github.com/uclat-lab/uclat-lab.github.io/tree/master/_posts) 
and click **Create new file**. 

![Screenshot-post-edit](assets/img/site_readme-05-create-post.png)

The filename must begin with the date in YYYY-MM-DD format, followed by a brief 
title delimited by hyphens and then the extension `.md`. The post must begin 
with these six lines:
```
---
title: 
author: 
layout: post
group: news
---
```
For `title: `, enter the post title as you want it to appear on the News page. 
For `author: `, enter your own name as it is spelled in 
[/_data/members.yml](https://github.com/uclat-lab/uclat-lab.github.io/blob/master/_data/members.yml). 
If you would like to include an image, upload a JPEG or PNG file to 
[/assets/img/](https://github.com/uclat-lab/uclat-lab.github.io/tree/master/assets/img) 
(ideally, with a width of 490 pixels) and include a tag in your post using the 
format:
```
![ALT-TITLE](/assets/img/FILENAME.png)
```
where for `ALT-TITLE` you put in a brief description and for `FILENAME` you 
enter the filename of the image you uploaded to 
[/assets/img/](https://github.com/uclat-lab/uclat-lab.github.io/tree/master/assets/img). 
(I suggest naming it something like "news_YEAR_key-words.png".)

When you're done, **commit changes**, using the green button to commit the file 
directly to the master branch and the description box below to leave a brief 
description.
