### 1. Explain File Attribute in details 

File attributes are the properties or metadata associated with a file, which describe its behavior, status, and permissions. These attributes help the operating system manage files efficiently. Common file attributes include:
- Name: The name of the file.
- Type: The file extension that defines the type of file (e.g., `.txt`, `.jpg`).
- Location: The path of the file on the disk.
- Size: The total size of the file in bytes.
- Permissions: Defines who can read, write, or execute the file.
- Ownership: Defines the owner and group of the file.
- Time/Date Stamps: Includes the time when the file was created, modified, or last accessed.

---

### 2. Explain File Operations in details. 

File operations refer to the actions that can be performed on files in an operating system. These operations include:
1. Create: Creates a new file.
2. Open: Opens an existing file for reading, writing, or appending.
3. Read: Reads data from a file.
4. Write: Writes data to a file or modifies its content.
5. Append: Adds data to the end of an existing file.
6. Close: Closes a file after use.
7. Delete: Deletes a file from the file system.
8. Seek: Moves the read/write pointer to a specific location in the file.
9. Rename: Changes the name of a file.

---

### 3. List out types of Directory Structures. 

Types of directory structures include:
1. Single-Level Directory: All files are stored in a single directory.
2. Two-Level Directory: Each user has their own directory.
3. Tree-Structured Directory: A hierarchical directory structure with directories and subdirectories.
4. Acyclic Graph Directory: Allows shared directories and files without cycles.
5. General Graph Directory: Allows shared files and directories with possible cycles.

---

### 4. Explain Tree structured Directories in details 

A tree-structured directory is a hierarchical file organization where each directory can contain files and subdirectories, similar to a tree. The root directory is the topmost directory, and subdirectories branch out from it. Each file in the directory can be accessed through its unique path.

Advantages:
- Hierarchical Organization: Files are better organized in a structured manner.
- Efficient Searching: Searching for a file becomes easier in the tree structure.
- User-Specific Directories: Each user can have their own directory for better management.

Example:
```
Root Directory
  |
  ├── Documents
  |    ├── file1.txt
  |    └── file2.docx
  |
  ├── Pictures
  |    ├── vacation.jpg
  |    └── birthday.png
  └── Music
       └── song.mp3
```

---

### 5. Explain all methods of Disk Space Allocation Method. 

Disk space allocation methods include:
1. Contiguous Allocation:
   - All blocks of a file are stored contiguously on the disk.
   - Advantages: Simple and fast for sequential access.
   - Disadvantages: Can lead to external fragmentation and may not be suitable for dynamically changing file sizes.

2. Linked Allocation:
   - Each file is a linked list of disk blocks, and each block points to the next.
   - Advantages: Eliminates external fragmentation.
   - Disadvantages: Slower access due to traversal and storage overhead for pointers.

3. Indexed Allocation:
   - A special block (index block) contains pointers to all the blocks of a file.
   - Advantages: Provides fast direct access to file blocks.
   - Disadvantages: Requires additional space for the index block.

---

### 6. Explain Physical structure of Hard Disk 

The physical structure of a hard disk includes:
- Platters: Circular disks coated with magnetic material that store data.
- Tracks: Concentric circles on the platters where data is written.
- Sectors: Smallest storage units, subdivisions of tracks.
- Cylinders: A collection of tracks across all platters at a specific radius.
- Read/Write Heads: Mechanism that reads and writes data on the platters.
- Spindle: The axis on which platters rotate.
- Actuator Arm: Moves the read/write heads over the platters to the correct track.

---

### 7. Explain SCAN Disk scheduling with example 

SCAN disk scheduling (also known as the Elevator Algorithm) moves the disk arm towards one end of the disk, servicing requests along the way, and then reverses direction. It provides better performance than FCFS and reduces the number of head movements.

Example:
- Disk request queue: `176, 79, 34, 60, 92, 11, 41, 114`
- Head starts at track `50`, direction towards higher numbers.
- Service order: `60 → 79 → 92 → 114 → 176 → reverse → 41 → 34 → 11`
- Total head movements: `(50 → 176) + (176 → 11)`

---

### 8. Explain C-SCAN Disk scheduling with example 

C-SCAN (Circular SCAN) disk scheduling is similar to SCAN but after reaching one end of the disk, the head returns to the beginning without servicing requests on the return trip. It provides a more uniform wait time compared to SCAN.

Example:
- Disk request queue: `176, 79, 34, 60, 92, 11, 41, 114`
- Head starts at track `50`, direction towards higher numbers.
- Service order: `60 → 79 → 92 → 114 → 176 → jump to 0 → 11 → 34 → 41`
- Total head movements: `(50 → 176) + (176 → 0) + (0 → 41)`

---

### 9. Explain File Protection 

File protection in Linux ensures that only authorized users can access and modify files. Protection mechanisms include:
1. File Permissions: Files have read, write, and execute permissions for the owner, group, and others.
2. Access Control Lists (ACLs): Provide more granular control over who can access a file.
3. Encryption: Files can be encrypted to prevent unauthorized access.
4. Authentication: Requires users to verify their identity before accessing a file.

Example of file permissions:
```bash
chmod 755 file.txt
```

---

### 10. Give meaning of .exe, .docx, .pdf, .zip, .jpg, .mp3 

- .exe: Executable file, used to run programs.
- .docx: Microsoft Word document file.
- .pdf: Portable Document Format, used for documents.
- .zip: Compressed file or archive.
- .jpg: Image file in the JPEG format.
- .mp3: Audio file in the MP3 format.

---

### 11. Consider the following disk request sequence for a disk with 200 tracks - 176, 79, 34, 60, 92, 11, 41, 114 and head pointer starting at 50. Find the number of head movements in cylinders using SCAN, C-SCAN, FCFS, and SSTF scheduling algorithm.

Given:
- Disk request sequence: `176, 79, 34, 60, 92, 11, 41, 114`
- Head pointer starts at track `50`.

#### 1. SCAN:
- Service order: `60 → 79 → 92 → 114 → 176 → reverse → 41 → 34 → 11`
- Total head movements: `(50 → 176) + (176 → 11) = 215`

#### 2. C-SCAN:
- Service order: `60 → 79 → 92 → 114 → 176 → jump to 0 → 11 → 34 → 41`
- Total head movements: `(50 → 176) + (176 → 0) + (0 → 41) = 267`

#### 3. FCFS (First-Come, First-Served):
- Service order: `176 → 79 → 34 → 60 → 92 → 11 → 41 → 114`
- Total head movements: `(50 → 176 → 79 → 34 → 60 → 92 → 11 → 41 → 114) = 499`

#### 4. SSTF (Shortest Seek Time First):
- Service order: `60 → 41 → 34 → 11 → 79 → 92 → 114 → 176`
- Total head movements: `(50 → 60 → 41 → 34 → 11 → 79 → 92 → 114 → 176) = 237`