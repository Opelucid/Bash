---
id: wwnxehu5kdfhc9apcai4n48
title: GNU Shell Intro
desc: ''
updated: 1690303261338
created: 1690298138019
---

## Beginner Commands
 1. ### man
    * manual for commands (better help)
    * example usage: ```man <command>```
        * you can also use ```tldr <command>``` for short examples of stuff
 2. ### ls
    * list all files a folder contains
    * if you add a folder name or path it prints that folder's contents
        * example: ```ls /bin```
 3. ### cd 
    * change directory; specify a folder to move into.
        * example: ```cd /downloads```
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
     * other examples of type searches are ```-type f``` which searches only files or ```-type l``` for symbolic links.
     * note that ```-name``` is case sensitive so instead utilize: ```-iname``` to perform case insensitive searches
     * you can also search under multiple root trees
          * example: ```find folder1 folder2 -name name_of_file.txt```
     * You can also exclude a path using ```-not -path```
     * Searching for files bigger than 100 Kilobytes and smaller than 1 megabyte
          * ```find . -type f -size +100k -size -1M```
     * More examples are linked in 
 12. ### ln 
     * used to create links within the Linux file system. effectively pointers to another file / a file that points to another file.
     * There are two major types of ln
         * Hard Links
             * rarely used; cannot be used to link to directories
             * cannot link to external file systems
             * "If you delete the original file, the link will still contain the original file content, as that's not removed 'til there is a hard link pointing to it."
             * The syntax for hardlinks are ```ln <original> <link>```
                * example: ```ln sean.doc newsean.doc```
         * Soft Links
             * more powerful!!
             * you can use these to link to other file systems and to directories
             * if the original file is removed the link is broken
             * The syntax for soft links are ```ln -s <original> <link>```
                * example: ```ln -s sean.doc newsean.doc```
                * something interesting to note, there is a  ```l``` flag if you list the file via ```ls -al``` and the file name will have an ```@``` at the end.
                * 
    