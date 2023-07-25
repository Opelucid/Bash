---
id: wwnxehu5kdfhc9apcai4n48
title: GNU Shell Intro
desc: ''
updated: 1690303261338
created: 1690298138019
---

## Top Layer
 1. ### man
    * manual
    * example usage: ```man <command>```
        * you can also use "tldr" for short examples
 2. ### ls
    * list all files a folder contains
    * if you add a folder name or path it prints that folder's contents
        * example: ```ls /bin```
 3. ### cd 
    * change directory; specify a folder to move into.
        * example: ```cd downloads```
 4. ### pwd
    * shows you place in directory. (use if lost)
 5. ### mkdir
    * create folders
    * example: ```mkdir Uni```
 6. ### rm
    * delete stuff!!!
    * example: ```rm -i sean.pdf```
    * works silently unless -i (prompts y or n if it should delete)
        * be careful with -rf 
        * ```-r ```- The option indicates recursive removal and helps remove non-empty directories.
        * ```-f``` :The option allows removal without confirmation, even if a file does not exist. 
        * sudo gives root access for this
 7. ### mv
    * move files around
    * example moving a .doc file to folder Uni: ```mv 'sean.doc' Uni```
    * If the last parameter is a folder, the file located at the first parameter path is going to be moved into that folder. In this case, you can specify a list of files and they will all be moved in the folder path identified by the last parameter
 8. ### cp 
    * copy files
    * example: ```cp 'sean.doc' seanie.doc```
      * seanie.doc here is the new name of the copied file while sean.doc is the original
    * to copy entire folders just add ```-r``` to recursively copy the entire folder's contents
 9. ### open 
    * opens files and or directories
    * weird example: ```open .```
        * the ```.``` symbol points to the current directory
        * the ```...``` symbol points to the parent directory
     * same comand can be used to run applications and files
        * example: ```open sean.doc```
 10. ### touch
     * you can create an empty file with touch
        * if the file already exists it opens the file in write mode and it will update the files timestamp
     * example: ```touch summit```
        * this creates a file called summit at the directory this is pointing to
 11. ### find
     * used to find files or folders matching a particular search pattern. It searches recursively by default.
     * example: ```find . -name '*.js'```
        * all files under current tree that have .js extension and print the relative path of each file that matches
          * we use quotes around special characters like ```*``` to avoid shell interpreting them.
     * example: ```find . -type d -name src```
          * this finds all directories under the current tree matching the name src
 12. ### 

    