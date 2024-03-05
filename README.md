# Python Algorithm for File Updates

## Project description
A company uses the IP addresses of employees to control who is able to access confidential internal data. This is controlled by the use of  an allow list, which lists the IP addresses of employees with access to the file. This file must be regularly updated and maintained. 
A separate remove list identifies IP addresses to be removed from the list for various reasons. This can be done by creating an algorithm in Python that checks the allow list file and the remove list to ensure that the IP addresses in the list are up to date and that employee access is correct.

## Open the file that contains the allow list

To begin, open the file: `allow_list.txt` as that contains the IP addresses that are allowed access. This is done by assigning the file name as a string as a variable called `import_file`. Then using a `with` statement to open the file itself into python. 

![1](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/99c57930-6d27-4176-926f-a7eb6c85a4da)
![2](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/cffa7a6c-5f18-4db8-89db-13ec32111a00)

The `.open()` function’s second parameter contains the `“r”` string which indicates that the file is being opened with the purpose of being read. 

## Read the file contents
To be able to actually read and interact with the contents of the file it needs to be converted into a string.  This is done by using the .read() method and assigning the file that was imported earlier to a variable. 

![3](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/c8e62642-79b2-4791-afa5-881538e78c76)

After applying the `.read()` method to the file and stating it as a variable, it becomes a string that can be read as a string format in the code. 

## Convert the string into a list
Now that the file is a string, it will state all the IP addresses on the `allow_list.txt`. However, in order to remove individual IP addresses from the list. The string must be converted to a list format so that each IP address is its own object. To do this, the ip_addresses that variable was defined in the previous step will go through the `.split()` method. This will convert each entry on the list that is separated by a space into its own element.

![4](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/88b01785-627c-49d7-93ad-4336063e56f6)

## Iterate through the remove list
Now that the IP addresses are individual elements in a list. Check them against the IP addresses in the `remove_list`. To do this we must create a `for` loop that will cycle through each `element` in the newly created list. For clarification, an `element` here is an IP address on the list.

![5](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/2010a6b6-5254-4fb3-a592-4300c8f2123b)

Then following that statement we’ll add the conditional that will check if an `element` matches an IP on the remove list, and this line of code will proceed to the next section if this condition is true.

## Remove IP addresses that are on the remove list
This part continues from the statement created in the previous section. 
For the purpose of this demonstration, we will just define the list with example IP addresses:

![5-5](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/7281f5ce-e332-496e-91e3-13fe0a426563)

Adding one final line to the for statement:

![6](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/8648f25b-a807-4621-ae2b-1e5cf2c4512e)

The line ip_addresses.remove(element) will remove an element from the ip_addresses list if the above line: if element in remove_list is true, which also means that an IP address from the remove_list matches with an IP address on the allow list. 
Update the file with the revised list of IP addresses 
Finally, after the IP addresses from the remove_list are taken out of the IP address list, we must place the new list of IP addresses back into the original file. First, we must put the list we had created back into a single string that can be put back into the text file. This will be done by using the .join() method with the ip_addresses. 

![7](https://github.com/RafUrera/Python-Algorithm-for-File-Updates/assets/161657613/ed93eb3e-9a82-47d5-a98c-78237557bf28)

Then a with statement is used again to open allow_list.txt. However this time, the ”w” parameter will be used. This indicates that the file can be used with the .write() function. This final line will replace the contents of the file with the revised IP addresses and update the employees that have access to the restricted data.

## Summary
This was a short breakdown and explanation of an algorithm that is used for a task that must be  done regularly. This Python code uses various methods and statements to automate repetitive tasks. 
