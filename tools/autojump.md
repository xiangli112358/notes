# Autoump
[Autojump](https://github.com/wting/autojump) is a enhancement of `cd` command tool. It is a faster way to navigate your file system, 
by maintaining a database of the directories you use the most from the command line. Autojump is not a replacement of `cd` command, 
directories must be visited first before they can be jumped to.

## Installation
### MacOS X
```
brew install autojump
```
To integrate with zsh, add the following line in .zshrc file.
```
[[ -s ~/.autojump/etc/profile.d/autojump.sh ]] && . ~/.autojump/etc/profile.d/autojump.sh
```

Note: *source the .zshrc file to update current session.*

## Usage
### Jump to a directory
```
j <directory>
```
The parameter *directory* can be part of the path, and you can type `tab` to complete automatically.

### Jump to a subdirectory
```
jc <subdirecotry>
```
You don't need to type the full name of the subdirectory.

### Open in file explorer
```
jo <directory>
```
This will not jump to the directory, but open the direcory in file explorer instead(for MacOS, it is Finder).

### Open a subdirectory in file explorer
```
jco <subdirectory>
```

### Show database entries and their key weights
```
j -s (or j --state)
```
The more often you visited a directory, the higher you got the weight.
 
### Remove unused entries
```
j --purge
```
If paths are no longer existed, they will be removed from the database.
