# Guide to write your Lab-book

[TOC]

## Directory structure

Create a directory structure as in the example found in ```/mnt/PALM_dataserv/DATA/Public/Labbook```

Remember to use a date followed by a title of what will be stored in that directory, as in ```2019_09_03_Create_Labbook```

Remember never to use spaces or wild characters (such as *&^$#) in folder or file names.

The directory looks like:

```sh
(base) marcnol@maupiti:~/PALM/Public/Labbook$ ls -lr
total 16
drwxr-xr-x 2 marcnol cbs 4096 Sep  3 12:50 2019_09_03_Create_Presentation_Group_meeting
drwxr-xr-x 2 marcnol cbs 4096 Sep  3 12:48 2019_09_03_Create_Labbook
drwxr-xr-x 2 marcnol cbs 4096 Sep  3 12:50 2019_09_03_Create_experiment2
drwxr-xr-x 2 marcnol cbs 4096 Sep  3 12:50 2019_09_03_Create_experiment1
```

if you want to look at how this looks, open this [link](./).

## Header file

The header file is a file that lives in the root of your directory structure, in this example this would be ```/mnt/PALM_dataserv/DATA/Public/Labbook```, and that contains links to your data and experiments.

For instance, let's say you have a project where you look for the transcriptional state of cells in chicken skin cells. In this case, everyday you will have different experiments performed and the images/videos/labbook pages for each day will be stored in a specific directory as described in the first section (e.g. ```2019_09_03_Create_experiment1```). After a while, it will be hard browsing folder per folder and file per file to find when you did each experiment. So this is where you header file comes from.

If you want to see an example of a header file, open this file:

```sh
/mnt/PALM_dataserv/DATA/Public/Labbook/project1.md
```

[Link to project1](/mnt/PALM_dataserv/DATA/Public/Labbook/project1.html)

## Markdown

How are labbook pages written? Word? OpenOffice? Google Docs? **You guessed: none of the above.**

Labbooks are written in Markdown, a very *easy to use* programming language that allows you to concentrate on writing. Here are some examples of what you can do with it:

### Getting Markdown

There are many applications that support Markdown. I use [Typora](https://www.typora.io/#linux), or [Haroopad](http://pad.haroopress.com/) or [Atom](https://atom.io/) for **offline** editing (my favorite).

But you can also use on-line editors such as (Dillinger)[https://dillinger.io/] or [StackEdit](https://stackedit.io/app#) or (HackMD)[https://hackmd.io/].

I recently installed [codiMD](http://192.168.6.30:3000/) in one of our servers. It is *supposed* to be great for document collaboration.

Do your shopping and stick to what you like the best.

### Writing text in markdown

#### Headers

To write headers of sections you just use '#'. For instance:

```markdown
# header 1

## header 2

### header 3

... you get the idea
```
#### Emphasis

This is even easier. For example

```markdown
**bold**
*italic*
9^th
```
will appear as

**bold**
*italic*

#### Lists

List are done by just using '-' For instance, the following

``` markdown
- item 1
- item 2
- item 3
	- item 3.1
	- item 3.2
	- item 3.3
```
will appear as

- item 1
- item 2
- item 3
	- item 3.1
	- item 3.2
	- item 3.3

An ordered list

```markdown
1. item 1
2. item 2
3. item 3
44. item 4
4. etc
```

 will look like:

1. item 1
2. item 2
3. item 3
4. item 4
5. etc



#### Images

Let's say you have an image, called pinguin.jpeg in your directory ```2019_09_03_Create_Labbook```

You can insert the image by typing

```markdown
![pinguin](./2019_09_03_Create_Labbook/pinguin.jpeg)
```

and it will appear as:

![pinguin](/mnt/PALM_dataserv/DATA/Public/Labbook/2019_09_03_Create_Labbook/pinguin.jpeg)

You can also add images from the internet by replacing the filename with a link.

#### Tables

Tables are easy, for instance, do

```markdown
| strains | Date | Procedence|
| --------|------|----------|
|sdsdnk| 20-09-76| Cozzlab|
| pyt233| 19-01-81| SherrattLab|
```

will appear as:

| strains | Date | Procedence|
| --------|------|----------|
|sdsdnk| 20-09-76| Cozzlab|
| pyt233| 19-01-81| SherrattLab|

and so on.


### Conversion

Markdown documents can be easily converted to word, html, latex, pdf using [pandoc](https://pandoc.org/MANUAL.html).

### Sharing

They can of course be easily shared provided you put the files within a Google Drive or Dropbox directory that you share with someone.

### Collaboration

I am still exploring the best ways for this. It seems HackMD (or their codiMD open source version) will be the best. Otherwise, straight ```git``` with Code reviews. But we are still exploring solutions for this.



## Mounting Google Drive and Dropbox

For Gdrive, follow the instructions [Gdrive Mounting](./Installing Google Drive Ocamlfuse on Ubuntu 18.04.md).

For Dropbox, follow the instructions here: [Dropbox Mounting](./Mounting Dropbox in Linux.md)



## Work in progress

This is a work in progress.

**Suggestions are of course more than welcome!**

That is all for now.
