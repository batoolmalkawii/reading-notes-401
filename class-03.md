# Explore the Tech!

## 1. Files in Python:
Files on most modern file systems are composed of three main parts:

  * Header: metadata about the contents of the file (file name, size, type, and so on).
  * Data: contents of the file as written by the creator or editor.
  * End of file (EOF): special character that indicates the end of the file.
   
 What this data represents depends on the _format specification_ used, which is typically represented by an extension.
 
 When you access a file on an operating system, a file path is required. 
 The file path is a string that represents the location of a file. It’s broken up into three major parts:

  * Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash `/` (Unix) or backslash `\` (Windows).
  * File Name: the actual name of the file.
  * Extension: the end of the file path pre-pended with a period (.) used to indicate the file type.
  
```
  /
│
├── path/
|   │
│   ├── to/
│   │   └── cats.gif
│   │
│   └── dog_breeds.txt
|
└── animals.csv
```

###### Problems with files:
  1. The representation of a new line or line ending.
  2.  the encoding of the byte data. An encoding is a translation from byte data to human readable characters.
      This is typically done by assigning a numerical value to represent a character. The two most common encodings are the `ASCII` and `UNICODE` Formats.
      
##### Opening and closing a file in Python:
When you want to work with a file, the first thing to do is to open it. This is done by invoking the `open()` built-in function. 
`open()` has a single required argument that is the path to the file. `open()` has a single return, the file object (Text files, Buffered binary files, Raw binary files).



  
  
  
