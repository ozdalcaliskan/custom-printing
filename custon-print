
import os
import time
import win32api

# In this algorithm, the data we want to print is ready as a .csv file. 

file_path = r'your\csv\folder\path\'
with open(file_path, "r") as file:
    print_list = file.read().splitlines()
  
# The folder containing the files to be printed.
folder_path = "Your\target\folder\path"

# A code sequence that searches the file names in the list we defined named 'print_list', one by one, and prints them in order as they are found.
for filename in print_list:
    file_path = os.path.join(folder_path, filename)
    if os.path.exists(file_path):
        win32api.ShellExecute(0, "print", file_path, None, ".", 0)
        time.sleep(5) 

#  This algorithm was written in a way that does not interfere with printer permissions. Since the order of the printouts is important for what I need,
# a three-second timeout has been added after each printing operation, taking into account the time it takes for the printer to accept documents of 
# different sizes into its memory.
