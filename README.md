# Building an EXT2 File System from Scratch

## Introduction
As part of the Systems Programming class I took, students were tasked with creating an EXT2 file system, as the semester-long project. We had some basic starter code and guiding help, but the bulk of developing everything was on us. This was an extremely challenging albiet frustrating experience.

## Beginnings
While we started with little to no knowledge, we quickly began learning about the many different key concepts of file systems. Those key concepts including inodes, directories, block allocation, disk partitioning, and more. Throughout the semester, as we learned more and more we added more and more onto our projects. 

## Disk Partitioning
One of the first practical steps of the project was partitioning the disk (of which we were provided by the professor). This involved using tools such as 'fdisk' to create dedicated partitions on our disk, in which the EXT2 file system would reside.
![EXT2 Block and Group](https://github.com/daniel-semenko/EXT2FileSystem/assets/74024282/7ea6ba50-603b-47a8-99a7-6e78debee7e7)

## Superblock Creation
The next step was to create the superblock, which is a pivotal part of the EXT2 file system. Creating this data structure properly involved key parameters such as block size, inode count, file system size, and more. Though challenging, we succesfully created the superblock, which heavily influences the design and performance of the file system.

## Block Group Organization
The next step we took was dividing the disk into block groups, which would optimize the performance and reduce fragmentation. This involved decisions around inode size, allocation rules, and inode numbering schemes, among other important items.

## Inode Table Design
Before we could fully implement and link our common linux commands, we had to design the inode table, which would define the structure for files and directories. This involved inode file sizing, allocation policies, numbering schemes, and more; needed to represent and manage objects in a file system.
![inode](https://github.com/daniel-semenko/EXT2FileSystem/assets/74024282/64b089e1-4897-446c-ab29-c128a5e58ea7)

## Diretory Implementation
Now, we could fully adapt directories and basic directory functionality. This involved creating the data structures and algorithms for managing files, filenames, and their inode numbers. This then could allow for the creation, reading, and updating/overwriting of entries.
![dir](https://github.com/daniel-semenko/EXT2FileSystem/assets/74024282/b08c008a-c730-4913-a514-b69e072cad97)

## Linux Utility
Finally, the implementation of the rest of the linux commands could be utilized, allowing for full Linux-style emulation of a EXT2 file system. These commands include cd, ls, pwd, stat, chmod, utime, mkdir, create, open, close, read, cat, rmdir, symlink, write, copy, and more.

These commands, along with those necessary for previously covered sections, all worked together to create a working emulation of an EXT2 File System.
