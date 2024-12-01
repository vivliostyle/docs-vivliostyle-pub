# Rename a Folder on GitHub

1. Make sure the "Code" tab is selected on the repository's main page. Click on the folder name you want to change (red circle). Here, we will change `chapter-3`.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-1.png)

2. You have navigated to the file list screen within the folder. To change the folder name, you will modify the path name from the repository to the file. Here, click on `section-1.md` (red circle).

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-2.png)

3. You have navigated to the file operation screen for `section-1.md`. Click the pencil icon on the right side of the screen (red circle).

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-3.png)

4. You will be taken to the editor screen. Click on the file name column (red circle ①) and move the cursor to the left end of the column as shown in the picture.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-1.png)

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-2.png)

5. Press the backspace key in this state. The folder column and file name column will merge into one, and the cursor will be displayed between the folder name and file name, making the folder name `chapter-3` editable.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-3.png)

6. Delete the `-3` part with the backspace key and enter `-100` instead.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-4.png)

7. Enter `/` in this state. The folder name has now been changed to `chapter-100`.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-5.png)

8. Click the "Commit Changes" button (red circle ②) to confirm the changes. You will return to the file operation screen for `section-1.md`. Click the repository name in the upper left corner of the screen (red circle).

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-5.png)

9. You have returned to the repository's main page. Let's reflect the folder name change in `vivliostyle.config.js`. Click the red circle.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-6.png)

10. You will navigate to the file operation screen for `vivliostyle.config.js`. Click the pencil icon on the right side of the screen (red circle).

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-7.png)

11. You have navigated to the editor screen. Change the previous folder name `chapter-3` to the new folder name `chapter-100` (red arrow). When finished, click the "Commit Changes" button to confirm the changes.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-8.png)

**Before Change**
```js
'chapter-3/section-1.md',
```

**After Change**
```js
'chapter-100/section-1.md',
```

12. Return to the repository's main page, and you will see that `chapter-100` has been added, and there are now two folders (red circle).

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-9.png)

13. Reload Vivliostyle Pub and check if the added `chapter-100/section-1` (red arrow) is displayed.

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-10.png)