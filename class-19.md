# Read:19 Summary
## Python Regular Expression
* `Regular Expressions` : often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not.
* They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files 
to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science
projects involving text mining.
* if you want to start using them in your Python scripts, you have to do `import re`
* Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.
* Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding,
they can be thought of as reserved metacharacters that denote something else and not what they look like.
### Grouping in Regular Expressions
* The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis () are
called groups. The parenthesis does not change what the expression matches, but rather forms groups within the matched sequence. You have been using 
the group() function all along in this tutorial's examples. The plain match.group() without any argument is still the whole matched text as usual.
### Greedy vs. Non-Greedy Matching
* When a special character matches as much of the search sequence (string) as possible, it is said to be a "Greedy Match"
* Although regular expressions are very powerful and helpful, be wary of long, confusing expressions that are hard for others, and also you to understand and maintain over time.
---------------------------------------------------------------------------------------------------------------------------------------------------------------
## shutil — High-level File Operations
* The `shutil` :  module includes high-level file operations such as copying and archiving.
### Copying Files
* `copyfile()` : copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.
* Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as 
new special files with copyfile().
* The implementation of copyfile() uses the lower-level function copyfileobj(). While the arguments to copyfile() are filenames, the arguments to 
copyfileobj() are open file handles. The optional third argument is a buffer length to use for reading in blocks.
### Copying File Metadata
* By default when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file
to another, use copymode().
### Working With Directory Trees
* `shutil` : includes three functions for working with directory trees. To copy a directory from one place to another, use copytree(). It recurses 
through the source directory tree, copying files to the destination. The destination directory must not exist in advance.
* copytree() accepts two callable arguments to control its behavior. The ignore argument is called with the name of each directory or subdirectory being 
copied along with a list of the contents of the directory. It should return a list of items that should be copied. The copy_function argument is called to
actually copy the file.
* To remove a directory and its contents, use rmtree().
* To move a file or directory from one place to another, use move().
### Finding Files
* The which() function scans a search path looking for a named file. The typical use case is to find an executable program on the shell’s search path 
defined in the environment variable PATH.
### Archives
* Python’s standard library includes many modules for managing archive files such as tarfile and zipfile. There are also several higher-level 
functions for creating and extracting archives in shutil. get_archive_formats() returns a sequence of names and descriptions for formats supported on
the current system.
* Use make_archive() to create a new archive file. Its inputs are designed to best support archiving an entire directory and all of its contents,
recursively. By default it uses the current working directory, so that all of the files and subdirectories appear at the top level of the archive. To
change that behavior, use the root_dir argument to move to a new relative position on the filesystem and the base_dir argument to specify a directory to 
add to the archive.
* This registry is different from the registry for creating archives because it also includes common file extensions used for each format 
so that the function for extracting an archive can guess which format to use based on the file extension.
* Extract the archive with unpack_archive(), passing the archive file name and optionally the directory where it should be extracted. If no directory is
given, the current directory is used.
### File System Space
* It can be useful to examine the local file system to see how much space is available before performing a long running operation that may exhaust that 
space. disk_usage() returns a tuple with the total space, the amount currently being used, and the amount remaining free.
--------------------------------------------------------------------------------------------------------------------------------------------------------------
### Watchdog
* Its Python API library and shell utilities to monitor file system events.
* Directory monitoring made easy with :
  * A cross-platform API.

  * A shell tool to run commands in response to directory changes.






























































