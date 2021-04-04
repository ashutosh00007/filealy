# filealy

The filealy is a node module built in pure javascript, which offers easy file manilputation with predefined functions and even gives a flexibility to create your own as it simplifies basic CURD operations of fs library with syntatical sugar.

# Getting Started

Install filealy using npm

`npm install filealy`

Import filealy

`const filealy = require('filealy");`

# filealy methods

All the methods need pathname of the file as parameter in `string` note: you need to come to root directory of your node.js project from filealy module by using `../../` followed by continuation of the file path.

eg. for a file named as text.txt in the root directory of you project path will be `../../text.txt`

## Simplified fs library methods

* *Read File* - filealy.getFileData(`string` pathname);
`var response = filealy.getFileData("../../text.txt");`

getFileData reads the file data and returns it in `string` fromat which can be manipulated asccordingly bu the user. 

* *Write File* - filealy.getFileData(`string` pathname,`string` data);
`filealy.writeFileData("../../text.txt","Data that need to be written in the file");`

writeFileData takes pathname in first parameter and data that need to be written in the second.

* *Append File* - filealy.appendDataAtlast(`string` pathname,`string` data);
`filealy.appendDataAtlast("../../text.txt","this data appends at the last in the file");`

appendDataAtlast appends the data at the last of the file.

* *Delete File Data* - filealy.removeFileData(`string` pathname);
`filealy.removeFileData("../../text.txt");`

removeFileData deletes the whole data in the file.

* *Delete File* - filealy.deleteFile(`string` pathname);
`filealy.deleteFile("../../text.txt");`

deleteFile deletes the file in the specified directory.

## File manipulation methods

* *Number of Charaters in a file* - filealy.numberOfAllChar(`string` pathname);
`var response = filealy.numberOfAllChar("../../text.txt");`

numberOfAllChar returns the number of `char` in a file, return type `int`.

* *Number of Charaters in a file without space* - filealy.numberOfAllChar(`string` pathname);
`var response = filealy.charWithoutSpace("../../text.txt");`

charWithoutSpace returns the number of `char` in a file excluding spaces, return type `int`.

* *First Charater* - filealy.firstChar(`string` pathname);
`var response = filealy.firstChar("../../text.txt");`

firstChar returns the first `char` in the specified file.

* *Last Charater* - filealy.lastChar(`string` pathname);
`var response = filealy.lastChar("../../text.txt");`

lastChar returns the last `char` in the specified file.

* *First Word* - filealy.firstWord(`string` pathname);
`var response = filealy.firstWord("../../text.txt");`

firstWord returns the first word in the specified file as `string`.

* *Last Word* - filealy.lastWord(`string` pathname);
`var response = filealy.lastWord("../../text.txt");`

lastWord returns the first word in the specified file as `string`.

* *Count words* - filealy.wordsCount(`string` pathname);
`var response = filealy.wordsCount("../../text.txt");`

wordsCount returns the the number of words persent in the specified file as `int`.

* *Lines words* - filealy.linesCount(`string` pathname);
`var response = filealy.linesCount("../../text.txt");`

linesCount returns the the number of lines persent in the specified file as `int`.


* *Charater on the placeValue* - filealy.placeCharater(`string` pathname,`int` placeValue);
`var response = filealy.placeCharater("../../text.txt",3);`

placeCharater returns the the `char` present on the specified `int` place in the file.

* *Word Present* - filealy.isPresent(`string` pathname,`string` value);
`var response = filealy.isPresent("../../text.txt","Hello");`

isPresent returns the the `boolean` value to indicate weather the string is present in the file or not.

* *Replace first word occurance* - filealy.replaceWord(`string` pathname,`string` valueTobeReplaced,`string` replacingValue);
`var response = filealy.replaceWord("../../text.txt","Hello","world");`

replaceWord replaces the first word occurance in the file which is specified in the second parameter and replaces it with the third parameter word of the function.