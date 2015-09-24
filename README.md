# GitBook for The Last Mile

This fork of GitBook includes minor changes to make the app suitable for use generating text-based curriculum for in-prison educational programs. The original site for GitBook can be found [HERE](https://github.com/GitbookIO/gitbook)

This fork has a version number `5.0.0` to facilitate linking this fork as the build version in the CLI.

This README includes barebones instructions for using this fork of Gitbook to locally generate written curriculum material for [The Last Mile](https://thelastmile.org/).

## How to use it:

### Install GitBook CLI

GitBook can be installed from **NPM** using:

```
$ npm install gitbook-cli -g
```

### Install the GitBook Editor (GUI)

This step is not mandatory, but *highly* recommended because it sure is nice and will make your life easier. There is no need to create an account since you will be working strictly offline. This tool is very intuitive, and the docs are [HERE](http://help.gitbook.com/)

Get the editor [HERE](https://www.gitbook.com/editor)

When you install GitBook Editor, it will create the following directory under your main user path:

```
user/GitBook
```
Navigate into this directory and clone the Last Mile version of the GitBook repo:

```
git clone https://github.com/thelastmile/gitbook.git ./gitbook
```
Last, you will need to run the following command to use this version in gitbook-cli:

```
$ gitbook versions:link 5.0.0 ./gitbook
```
Now the version tag `5.0.0` wil be associated with the `./gitbook` folder.

You can uninstall it using: `gitbook versions:uninstall 5.0.0`.

## Using GitBook Editor

When you create a new 'Book' in GitBook Editor, a folder is created on the path:

```
user/GitBook/Library/Import/new-book-name
```

You can serve a repository as a book by navigating into the `book-name` folder and using:

```
$ gitbook serve
```

Or simply build the static website using:

```
$ gitbook build
```
This will create a new folder `_book` under the `book-name` folder with the fully rendered html version of your book.

## If you Simply *Must*... 
### To use GitBook from the command line:

Create the directories and files for a book from its [SUMMARY.md](https://github.com/GitbookIO/gitbook#book-format) file (if existing) using

```
$ gitbook init
```
You can then work with your text editor to your heart's content, and use the `serve` and `build` processes listed above.
