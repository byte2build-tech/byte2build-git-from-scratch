# Diff and Patch Commands

This file contains the commands used in the Byte2Build tutorial to demonstrate how file differences are identified and applied using `diff` and `patch`.


## View File Contents


cat b2b_v1.txt


Displays the contents of the original version of the file.


cat b2b_v2.txt


Displays the contents of the modified version of the file.

---

## Compare Two Files

h
diff b2b_v1.txt b2b_v2.txt


Compares the two files line by line and shows the differences.

* Lines starting with `<` belong to the original file.
* Lines starting with `>` belong to the modified file.
* Indicators such as `2,5c2,5` show which line ranges were changed.

---

## Compare Files Using Unified Format


diff -u b2b_v1.txt b2b_v2.txt


Displays the differences in **unified format**, which is easier to read.

* Lines starting with `-` were removed from the original file.
* Lines starting with `+` were added in the modified file.
* Unmarked lines represent unchanged content and provide context.

Unified format is commonly used in patches and version control systems.

---

## Create a Patch File


diff -u b2b_v1.txt b2b_v2.txt > b2b_change.patch


Creates a patch file containing all the differences between the two file versions.

---

## Apply the Patch


patch b2b_v1.txt < b2b_change.patch


Applies the changes stored in the patch file to the original file.

The `patch` command reads the differences and updates the file accordingly.

---

## Verify the Changes


cat b2b_v1.txt


Displays the updated file after applying the patch.


## Summary

The `diff` command identifies differences between file versions, while the `patch` command applies those differences automatically. This mechanism forms the foundation of how modern version control systems track and apply changes.
