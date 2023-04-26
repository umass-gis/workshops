---
layout: default
title: Filepaths in MacOS
nav_order: 10
has_children: false
---

# Filepaths in MacOS
{: .no_toc }

How to save, locate, organize, move, and delete files on a Mac
{: .fs-6 .fw-300 }

This tutorial was created on Mac OS Ventura. Depending on your specific operating system, some options may appear differently on your machine, but the general processes should be similar if not the same.
{: .note}

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Introduction

In this tutorial, you'll learn how to:

* use Spotlight
* navigate Finder
* create folders
* save and copy files
* move and manage multiple files
* delete files

Smoothly operating and navigating your computer's file storage system is a fundamental skill for anyone who uses computers. On Mac OS, the hierarchical (or "nested") file system has three basic domains, Local, System, and User.

<img src="media/file_system_map.png" alt="MAC OS System Map" width=300>

[Image: Apple Inc.](https://developer.apple.com/library/archive/documentation/FileManagement/Conceptual/FileSystemProgrammingGuide/FileSystemOverview/FileSystemOverview.html)


The term "file path" refers to the specific location of a file or folder within the computer's directory. If you know a file or folder's path, you can navigate to its location using Finder, or by searching its name. The forward slash "/" symbolizes the hard drive ("Macintosh HD") which is the base or "root" directory on Mac OS. Absolute file paths begin with "/", list all child directories, and terminate at the file or folder of interest. Relative file paths are written relative to their enclosing folder, and may begin further "down" in the directory. For example, the absolute path of "hello_world.txt" is

```
/Users/UMass/Documents/TextFiles2021/hello_world.txt
```

From "Umass", the relative path would be:

```
Documents/TextFiles2021/hello_world.txt
```

With the exception of the Applications folder (in the Local Domain), most users should avoid manipulating any files in the "System" domain, and should only work within the "User" domain.

---
## Using Spotlight

You may search all your files, applications, and folders directly by typing search terms into Spotlight. You may search for file types by typing the file extension in (e.g. .png, .docx, .xlsx., etc.), and all files with that type will be shown.

Similarly, searching for "Documents", will return not only the folder(s) called "Documents", but also any files containing the word "documents". This can be useful for finding files where you know some of the contents, but not the file name itself. For example, if you had a word document that included in its body "Roses are red, violets are blue", but the file was named "Untitled_document" and you were unaware of its location, you could search "Roses are red, violets are blue" and Spotlight will search through your computer, find any documents that include that exact text, and will show "Untitled_document".

Spotlight also automatically searches the internet for your search term, and will show search results categorized by the type of file it is displaying. It is a powerful tool that's worth becoming acquainted with.

1. Spotlight may be opened in one of three ways:
    1. **Click the small magnifying glass icon near the upper right corner of the Menu Bar (pictured below)**
    1. Hold the "Command" key, and press the space bar once, then release the "Command" key.
    1. Open any Finder window, and type into the search bar in the upper right corner of the window, this allows searching, but the results are returned within a Finder window, not a spotlight window. If using this option, the default search is a spotlight search of the entire computer, but the option will appear to instead search only the current directory (folder), which can be very useful when you know a files location, but don't know its name. This option will not search the internet.

    ![74!](media/74_spotlight.png "74")

1. A new spotlight search bar should appear. **Search "documents"**

    ![75!](media/75.png "75")

    It may take a moment to index and return results, but spotlight should now show a "Documents" folder. ***A single click on any of these items will open the file/folder.***

    ![76!](media/76.png "76")

1. **Scroll to the bottom of the spotlight window, and click "Search in Finder"**

    ![77!](media/77.png "77")

    A new Finder window will appear, showing the results of your spotlight search.

    ![78!](media/78.png "78")

1. If you want to know the file path, click the file of interest, and if the Path bar is toggled on, you will see the file path appear at the bottom of the Finder window. You've now searched and located an item using spotlight, congratulations!

    ![79!](media/79.png "79")

---
## Configuring Finder
{:toc}

To navigate through Mac's file system, you will primarily rely on Finder. Finder has multiple view options, some of which can be customized further for efficient file management. This section presents the various view options available within Finder, and provides examples of when each view may be the most useful.

Change the View Options in Finder to make it easier to view files and navigate through folders.

**1.** Open the Finder application by clicking any blank area on the Desktop.<br>
**2.** From the Menu bar, select **Go**

![1!](media/1.png "1")

**3.** From the dropdown menu, select Computer

![2!](media/2.png "2")

**4.** A new finder window will appear, showing "Macintosh HD", and "Network" icons. Currently, the finder window is set to display items in "icon" view, indicated by the four small highlighted boxes at the top of the finder window.

![3!](media/3.png "3")

### List View
{: .no_toc}

**5.** To toggle to "list" view, **select the symbol with the three small horizontal lines**. Notice that now, columns titled "Date Modified", "Date", and "Kind" have appeared. This is an excellent view option if you have many items in a folder and want to organize or view them with a little more detail. These view options are also available from the Finder Menu bar, under "View"

![4!](media/4.png "4")

**6.** Once in List view, select "View" from the finder menu bar.

![20!](media/20.png "20")

**7.** Select "Show View Options"

![21!](media/21.png "21")

**8.** A dialog box should appear showing check-boxes to toggle specific attributes. Check Date Created, Size, and Date Modified.

![22!](media/22.png "22")

**9.** In the desktop shown below, the items are organized by the date they were modified; the most recently-modified appearing at the top. This is indicated by the text "Date Modified" being highlighted. Double-clicking "Date Modified" will reverse the order. The same is true of all column headers.

![23!](media/23.png "23")

**10.** To organize files based on their size, **click "Size"**. Notice that only files have associated sizes. The folders contain files (that all have sizes), but finder only reports size for files, not folders. Note: to see the total size of a folder, right-click the folder, and select "Get Info" from the dropdown menu.

![24!](media/24.png "24")  

**11.** The desktop items are now organized by their size. This can be especially helpful when cleaning out files to save space.

![25!](media/25.png "25")

### Column View
{: .no_toc}

**12.** To toggle to "column" view, **select the symbol with three vertical lines**. This is an excellent view to use when navigating through Macs' nested file structure. Once a directory is selected, users may navigate by clicking with their cursor, or by using their directional arrow keys.

![5!](media/5.png "5")

### Gallery View
{: .no_toc}

**13.** A "gallery" view is also available, which shows a short summary of the file, and displays a large icon. To activate "Gallery" view, **select the right-most symbol**, which is a small rectangle with three dots beneath it. Afterwards, switch back to Icon view.

![6!](media/6.png "6")

### Toggling the Path Bar
{: .no_toc}

**14.** At the bottom of the displayed Finder window, the absolute path of the current directory is shown.

![8!](media/8.png "8")

**15.** To toggle this "Path Bar" on or off, **select "View" from the finder menu bar**.

![9!](media/9.png "9")

**16.** From the dropdown menu, **select "Hide/Show Path Bar"**. Please toggle the path bar on for the duration of this tutorial. It can be useful to see full file paths while navigating through finder. This way, if you are ever in doubt of a file's location, you will have quick access to its parent directories. **Note: Clicking a folder in the file path bar navigates to that directory.**

![10!](media/10.png "10")

---

## Exploring the Directory Structure
{:toc}

This section presents Mac OS system domains, describes their role and position in the directory structure, and provides tips on how and when to use these folders.

### Macintosh HD (Hard Drive) "/"
{: .no_toc }

**1.** Double-click "Macintosh HD".

![11!](media/11.png "11")

**2.** This is the "root" (or base) directory, symbolized by "/" in all absolute file paths. All files contained on your computer are held in this location. They are in one of four locations, "Applications", "Library", "System", or "Users"

![12!](media/12.png "12")

### Library
{: .no_toc }

**3.** Double-click the Library folder, but **do not make any changes to this folder**.

![13!](media/13.png "13")

**4.** **IMPORTANT NOTE** Unless you are advised by an Apple representative, or someone with a high level of technical knowledge, **never add, delete, manipulate or change any files in this location**. The files contained in the Library directory are used for basic processing tasks, and changing anything in this folder (including adding folders), could disrupt your computer, or stop it from working entirely.
{: .warn}

![14!](media/14.png "14")

**5.** In the upper left corner of the finder window, **select the left arrow to navigate "backwards"**, to the directory we were last in, called "Macintosh HD". These arrows allow users to toggle between the two most recently-viewed directories.

![15!](media/15.png "15")

### Applications
{: .no_toc }

**6.** From "Macintosh HD" **Double-click the "Applications" folder**.

![16!](media/16.png "16")

**7.** **Select "List" view** to show item details. This is the default save/installation location for any applications that are installed on your machine. If you download an app from the app store, and install is using default settings, you will be able to run the application by locating it in this directory and double-clicking it. "Downloads" is the default save location for most software downloaded through an internet browser, and "Applications" is the default installation location.

![17!](media/17.png "17")

### "Favorites" Bar (Quick Access)
{: .no_toc }

**8.** On the left-hand side of all finder windows, underneath the red, yellow, and green buttons, several "Favorite" directory locations appear in blue text. Users can also access the "Applications" folder by **clicking "Applications"** from Favorites.

![18!](media/18.png "18")

**9.** Select "Desktop" to show the items present on your desktop and **select list view**. In the picture shown, the user has 7 folders, and 2 files on their desktop.

![19!](media/19.png "19")

---
## User Domains
{:toc}

With the exception of Applications, the default save location for all files in a Mac environment is within the Users domain. (It is useful to store applications in the "Applications" folder within the system domain; this enables applications to be run from any new/additional user accounts you create). Other than applications, all files should be carefully organized within the User domain.   

**1.** To examine the set of User directories, open Macintosh HD and **double-click the folder of the user you are currently logged in to.** You will be able to tell which user you are in because the current User folder will have a small "Home" or "House" symbol on it. If you have any doubt about which User account you are currently in, click the apple-shaped icon in the upper left corner of the screen, and look at the bottom "log out of..." text. What follows "log out of..." will be the name of your current user.

![26!](media/26.png "26")

**2.** Now that we're viewing the main User folder, several sub-folders should appear. With the exception of "Zotero" and "test_directory", all other folders should be present in your User folder. Take note of the "Downloads" folder. This is the default save location for any data, folders, or files downloaded from the internet. If you download a photo, music file, or video file, it is possible (depending on your system settings) that the file will be saved in "Movies", "Music", or "Pictures" -- this may be a good place to check if a download is not showing up in the "Downloads" folder. **Note: it is generally best-practice to avoid leaving items in your downloads folder; ideally they would be filed into some logical system of organization within your directories immediately after download.*** See below for more information.

![27!](media/27_download.png "27")

---

## Best Practices in File Management

All files should periodically be backed up ("copied") to an external hard drive. Particularly important files and folders should also be backed up to the Cloud. In general, weekly updates should suffice. Check out [Time Machine, Apple's native back-up software.](https://support.apple.com/en-us/HT201250) to automatically back up all user settings, applications, data, files, and folders, every time you connect your external drive.
{: .warn}

**1.** In order to simplify file paths and make your directories easier to navigate, we suggest that you use "Documents" as the main folder in which all other files and folders are kept. **Double-click "Documents" to view this directory.**

![29!](media/29.png "29")

If the machine were for Graduate School, Work, and Personal use, one might add the following folders in Documents to begin organizing files (potential subfolders are shown as nested bullets):

* Pictures
  - pics_2023 (with subfolders like "Cape Cod Vacation", or "Dog Pictures")
  - pics_2022
* Videos_2023
  - vid_2023
  - vid_2022
* workDocuments_2023
  - Client_list
  - wd_q1
  - wd_q2
  - wd_q3
  - wd_q4
  - WorkDocs_archive (with subfolders for previous years)
* PersonalDocuments_2023
  - Taxes_2023
  - Receipts_2023
  - Poems_2023
  - Misc
* GradSchool_docs
  - Fall_2023 (Could include subfolders such as "Econ101", "Assignments", etc.)
  - Winter_2023
  - Spring_2023
* GradSchool_data
 - Modeling_data
 - Data_Documentation

Ensure that your directory structures ***makes sense for you and how you plan to use your computer***. For example, someone using advanced softwares with large volumes of complex data will need a sophisticated set of directories, whereas simple media files like photos, music, and documents, may be stored using more only a few folders. If users neglect to set up directories that align with their computer use, over the weeks and months they may spend ***many hours*** sifting through their files to find the one(s) they need. It is generally worth it to spend some time creating a logical directory for yourself, and then to continually tinker with and update it as needed. Use short, descriptive file names, and when the file is important, it doesn't hurt to include the date in the the name (e.g. "smith_resume_04_28_23" or "sResume_042823").

---

## Practice: Creating Folder and Files

In this section, users practice creating a new folder and text file, and then save to the recently-created folder. Various methods are discussed, and the each process is described in detail.

### Create a New Folder
{: .no_toc }

**1.** While in the documents folder (or with the Documents folder selected), click "File" from the menu bar.

![30!](media/30_new_fold.png "30")

**2.** From the dropdown menu, select "New Folder".

![31!](media/31.png "31")

**3.** A new folder named "Untitled Folder" will be added to the Documents directory. **Single-click "Untitled Folder"** to highlight it.

![32!](media/32.png "32")

### Rename a Folder
{: .no_toc }

**4.** With the Untitled Folder highlighted, **press "Enter" on the keyboard to select the text.** The text should now appear highlighted. **Rename the file to "a_new_folder", and press enter on the keyboard.** It's best to avoid including spaces in file and folder names, as some applications may have difficulty reading those files. That said, if most of your computer use is media and document-based, and you don't use advanced software, spaces will likely not be a problem.

![33!](media/33.png "33")

**5.** "a_new_folder" should now appear near the top of the documents folder, depending on how other items in the folder are named.

![34!](media/34.png "34")

### Create a Text File
{: .no_toc }

**6.** Open "Applications" from Favorites by single-clicking "Applications".

![35!](media/35.png "35")

**7.** Open "Text Edit".

![36!](media/36_txt.png "36")

**8.** With Text Edit open, select "File" from the menu bar.

![37!](media/37.png "37")

**9.** From the dropdown menu, click "New".

![38!](media/38.png "38")

**10.** Type something in the new Text Edit window.

![39!](media/39.png "39")

### Save to a Specific Folder
{: .no_toc }

**11.** With your altered Text Edit file open, **select "File" from the menu bar**.

![40!](media/40.png "40")

**12.** From the dropdown menu, **click "Save"**.

![41!](media/41.png "41")

**13** A new Save dialog box should open. The default save location is your most recent save location. For example, if the last place I saved something to was /Users/johnslaff/Music, "Music" would be selected instead of "Documents", as shown below. The view options (Icon, List, etc) are available to the left of the currently-selected directory. **Rename your file, and click the blue button (with little white arrows) directly next to the save location** to show additional directories. The white arrow next to the current directory hides and expands the navigator portion of the dialog box. The search bar allows users to search the current directory.

![45!](media/45.png "45")

**14.** Select your User account.  

![46!](media/46.png "46")

Your navigation window should now show your User directory and all its subfolders (if in column view).

![47!](media/47.png "47")

**15.** Select documents. Notice that each time you select a new folder, the current save location listed at the top of the dialog box changes.

![48!](media/48.png "48")

**16.** Select a_new_folder.

![49!](media/49.png "49")

**17. Press enter or **click the blue "Save" button** at the bottom right.

![50!](media/50.png "50")

Congratulations, you just created and saved a new file to a new folder!

![53!](media/53.png "53")

---
## Practice: Copying, Moving, and Deleting Files

Fundamental computer skills rely on the ability to efficiently move, copy, and remove/delete files. In this section, users gain some practice with these skills, and several different methods are demonstrated.

### Selecting Multiple Files
{: .no_toc }

Multiple files may be copied, moved, or deleted at once. To select all files in a directory, hold the "Command" key and press the "a" key on the keyboard.

To select multiple files in list or column view, highlight the first file by single-clicking it, then hold the "Command" key, and select additional files with a single click. Each new file will be added to the selection. Let up on the "Command" key when finished adding files, once you have released the Command key, you may hold it again and click a highlighted file to deselect it. The remaining selected files will remain highlighted/selected. Alternatively, after selecting your the file, holding the "Shift" key instead of the "Command" key will select all files between the first and second selections. This is a convenient way to bulk-select files. In Icon view, use the above methods, or click and drag a rectangle around the items you want to select.

**1.** Create a new folder in Documents, and then **select File from the menu bar**.

![59!](media/59.png "59")

**2.** From the drop down menu, **select "New Finder Window"**.

![60!](media/60.png "60")

**3.** A new Finder window should appear. Navigate to your new folder and resize the windows so you can see both at once.

![65!](media/65.png "65")

### Copying Files
{: .no_toc }

**4.** Right-click your file and select "Copy" from the dropdown menu.

Alternatively, you may select the file, hold the "Command" key, and press the "C" key (you may then release the "Command" key). Additionally, you may select the file, and then ***from the menu bar*** click "File", and select "Duplicate" from the dropdown menu. Note: "Duplicate" will add a new copy of the file to the directory in which the original file resides, "Copy" adds the file to your clipboard so it may be copied/added to any directory.

![66!](media/66.png "66")

**5.** Right-click anywhere in your original folder (the one from which the file came), and select "Paste" from the dropdown menu.

![67!](media/67.png "67")

A new copy of your file should be added to the directory.

![68!](media/68.png "68")

### Moving Files
{: .no_toc }

**6.** Click and drag the copied file into the new folder. (To click and drag: Hover over the file of interest, depress the left-click, and then without releasing, move the cursor--the file will move with the cursor--and release the mouse button/trackpad button when you are hovering over the new save location). Note: files may be copied or moved into folders directly, it is not necessary to open a new window with the folder you'd like to save to, you may drop directly into the folder icon and the files will be added to that directory.

![69!](media/69.png "69")

### Deleting Files
{: .no_toc }

**7.** Right-click the file you wish to delete, and **click "Move to Trash" from the dropdown menu.**

![70!](media/70.png "70")

**8.** Click the trash can icon to open up the Trash and view its contents. From here, files may be moved and added back to your file system if desired. To empty the trash and permanantly delete the enclosed items, click the button labeled "Empty" in the upper right corner of the Trash window.

![71!](media/71.png "71")