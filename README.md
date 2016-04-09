# Note add-on for todotxt

This add-on allows to keep notes attached to tasks. Just one note per task is allowed.

## Adding, editing notes

* `note ITEM#`. Adds a new note to task ITEM# and gives the chance to edit it, If note exists, Opens the note related with task ITEM# in editor.

## Example of use

	$ todo.sh ls
	1 Cook cake for birthday party
	2 Fix bicycle
	--
	TODO: 2 of 2 tasks shown
	
Say you're collecting recipes to prepare the cake from task 1 and want to write a note with the links to that recipes:

	$ todo.sh note 1
	1 Cook cake for birthday party note:cUn.txt
	TODO: Note added to task 1.
	Edit note?  (y/n)
	y

At this point, an editor is opened where you can enter any information related with task 1.

Perhaps you want to edit the note to add something else, then `todo.sh note 1` would open again the editor.

## Installation

Copy the `note` files in this directory to your add-ons folder.

## Configuration

You can change the note file extension by adding an entry to your `todo.cfg` file:

```
# Note file extension
export TODO_NOTE_EXT=.md
```
