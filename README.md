# Overview

Plugin is based on go pinboard for Alfred, from Hamid Ghadyani https://bitbucket.org/listboss/go-pinboard/wiki/Home

Pinboard for cerebro is a front end for Pinboard that allows you:

 * search
 * filter by tags
 * add public bookmarks
 * add private bookmarks
 * set a new bookmark as To Read
 * delete a bookmark
 * get the selected text as the bookmark description (see Syntax)
 * _interact with: Safari, Google Chrome, Google Chrome Canary, Chromium, Webkit and Firefox_

# First Run

Before running the workflow you need to set your Pinboard API Token:

To get it go to your Pinboard account and copy the API in Settings>Password

To enter it open Alfred Preferences>Workflows then select Pinboard then, finally, click in Configure Workflow and Variables (as seen below):

### Workflow Preferences

Follow the instructions there and the workflow should be ready to use.

# Usage

If you need help show Alfred and type the keyword phelp

## Search

Search will always look for URL, title, description and tags.

### Basic search

show Alfred and type the keyword ps
type your query e.g. ps apple

### Filtering by tags

show Alfred and type the keyword ps
type a hash sign and select a tag from the list (autocomplete) e.g. ps #tag1 #tag2 :
after the colon type your query e.g. ps #tag1 #tag2 :apple

### Actions

return key: open the bookmark
option key: delete the bookmark (you may need to manually reload the local cache)

## Add

### Public, Private and To Read Bookmarks

The workflow will list always two options:

Add Public Bookmark to Pinboard
Add Private Bookmark to Pinboard
Holding Command key will add it as an unread bookmark.

Note: make sure your Browser is the front most window then use the keyword pa

Note: Firefox may need that you reload the page. Anyway, the workflow always show the URL so you can check if it is right or not.

### Last Used

The workflow also saves the last command (Last Used item) so you can easily replicate. And with a hotkey you can add a bookmark even without any interaction at all.

### Syntax

You can optionally add tags and a custom description.

To add tags simply type a hash sign and select it from the list (autocomplete) e.g. pa #tag1 #tag2 :

After the colon, as seen above, you can optionally type the bookmark description e.g. pa #tag1 #tag2 :great workflow

And in order to get the selected text as the bookmark description type enclosed brackets after the colon e.g. pa [] or pa #tag1 #tag2 :[]

To add just a description just type it after the keyword e.g. pa great workflow

## Hotkeys

Search, Add and Last Used have also a hotkey that you can set in Alfred Preferences.

# Local Bookmark Cache

In order to make things a bit faster, the workflow caches all your Pinboard bookmarks and tags.

However, due even Pinboard API limitations the workflow will not, for now at least, update the cache automatically.

However, if your cache is more than one day older the workflow will let you know.

Anyway, you can use the keyword preload to manually update the local cache.
