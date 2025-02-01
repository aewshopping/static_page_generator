# Text file viewer

## What does it do? 

Loads a bunch of text files selected by you from your computer or phone, and outputs them in their entirety to the webpage - the contents of each text file are initially hidden in details elements.

It parses each file to look for tags. A tag is a # followed by a word, like this: `#tag`. You can then filter the notes by selecting tags.

It also makes a very basic attempt to parse the text from markdown to html in the normal way.

I called it a static file generator because the inspiration was partly from static site generators that generate lots of web pages, often from text files.

## What doesn't it do

You can't edit any text files, just view them.

Neither does it store any meta data about the files. All the information used is contained within the text files that you load. This is deliberate to maintain portability.

It doesn't communicate with a server: you could download the index.html file and use it without any internet connection.

I'm not sure how many text files it will happily load but 200 is no problem at all. I guess up to 1,000 normal length files would be fine and beyond this I'm not sure.

## Why bother? 

I store most of my notes as plain text files. It would be nice to organise them using something like obsidian. But you can't always install it in every environment. But you can always just click on an html file.

## How to install it

Download index.html and and click on it. (You should probably have a look through the code first to check your are comfortable that it isn't doing anything dodgy).

It is also deployed from GitHub pages in the normal way and you will be able to find a link to it somewhere around here.

## Useful things to know

### Tag taxonomy 

If you enter a tag like this: 

#favorite/tag

A `favourite` category will be created, and the `#tag` will be associated with it.

Only one category level is supported, so

#star/favourite/tag will probably not work.

### Lower case tags

All tags and categories are converted to lower case. 

### Extremely basic markdown

The markdown parsing is very simple. Only one level of list nesting for example. Links are not supported. Things will break, particularly on the first and last lines...

You could have a look at something like this if you wanted to improve the markdown parsing: [https://github.com/jozdk/simple-markdown-parser/tree/main](https://github.com/jozdk/simple-markdown-parser/tree/main).

### Colour modes

You can choose from two colour modes: snow or glow. 

### Filtering options

The tag filter can be set to either an AND filter (every tag must be present for the text file to show). Or an OR filter (at least one tag must be present in the text file).

