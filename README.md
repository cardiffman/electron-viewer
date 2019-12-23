# electron-viewer
A text file viewer using Electron-js

This project demonstrates how to use electron to view a plain text file.

- The file is streamed using fs.createReadStream so that only the part of the file in the DOM and a
stream chunk of the file are in memory
- The DOM manipulation is done by building a PRE element out of the DOM and then adding it. This avoids
reflows during the loading process.

## Problems:
- 100MB files may not work or it may depend on your RAM/swap whether it works or not.
