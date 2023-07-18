## File Sorting and Categorization using Python

This Python code allows you to sort and categorize files in a folder based on their last modified date and file type. The code uses the `os` and `shutil` modules to interact with the file system and perform file operations.

### Prerequisites

Before running the code, make sure you have Python installed on your system. The code is compatible with Python 3.

### Instructions

1. Open the Python file containing the code or create a new Python file.
2. Copy the code into the file.
3. Modify the value of the `folder_path` variable to specify the path to the folder you want to sort and categorize.
4. Save the file.
5. Run the Python file using a Python interpreter.

### How it works

1. The code begins by defining a dictionary called `file_types` which maps file types (videos, songs, text files, and others) to their respective folder names.

2. It then creates folders for each file type if they don't already exist.

3. The `cutoff_date` is calculated as the current date minus one year using the `datetime` and `timedelta` modules.

4. The code iterates over each file in the specified folder using `os.listdir(folder_path)`.

5. For each file, it checks if it is a directory. If it is, the code skips to the next iteration.

6. It retrieves the file's last modified timestamp using `os.path.getmtime(file_path)` and converts it to a `datetime` object.

7. The code compares the file's modified time with the `cutoff_date`. If the file was modified after the cutoff date, it skips to the next iteration.

8. The file's extension is extracted using `os.path.splitext(file_name)[1]` and converted to lowercase.

9. Based on the file extension, the code determines the file type (videos, songs, text files, or others).

10. The code moves the file to its respective folder using `shutil.move(file_path, destination_folder)`.

11. Finally, the code prints a message indicating the file that was moved and its destination folder.

### Customization

You can customize the code to fit your specific needs:

- Modify the `file_types` dictionary: If you want to categorize files into different types or add new types, update the dictionary accordingly.

- Adjust the cutoff date: If you want to change the cutoff date for filtering files based on their last modified date, modify the `cutoff_date` calculation.

- Add more file types: If you have additional file types you want to categorize, extend the conditions in the file type determination section and update the `file_types` dictionary.

### Example Usage

```python
folder_path = '/path/to/folder'
categorize_files(folder_path)
```

Replace `'/path/to/folder'` with the actual path to the folder you want to sort and categorize. Run the code to sort the files in the specified folder based on their last modified date and file type.

That's it! You should now be able to use the code to sort and categorize your messy files based on their last modified date and file type.
