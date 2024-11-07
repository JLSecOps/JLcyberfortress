# Algorithm for file updates in Python

## Project description

In this project, I created an algorithm that automates the process of updating a file that contains an allowed list of IP addresses with access to restricted content. The task involves checking whether any IP addresses from a list of restricted addresses (remove\_list) are present in the allow\_list. If so, those IP addresses are removed from the file. The allowed list is then updated with the revised list of allowed IP addresses. This process is automated using Python functions and file-handling techniques.

## Open the file that contains the allowed list

In this task, I opened the file allow\_list.txt which contains the list of allowed IP addresses using the open() function. The "r" parameter indicates the file is being opened for reading purposes.

\# Assign \`import\_file\` to the name of the file   
import\_file \= "allow\_list.txt"

\# Assign \`remove\_list\` to a list of IP addresses that are no longer allowed to access restricted information.  
remove\_list \= \["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"\]

\# First line of the \`with\` statement to open the file  
with open(import\_file, "r") as file:  
    \# Read file contents in Task 2  
    ip\_addresses \= file.read()

## Read the file contents

Here, I used the .read() method to convert the file's content into a string and stored it in a variable called ip\_addresses.

\# Use .read() to read the imported file and store it in a variable named \`ip\_addresses\`  
with open(import\_file, "r") as file:  
    ip\_addresses \= file.read()

\# Display the contents  
print(ip\_addresses)

## Convert the string into a list

In this step, I used the .split() method to break the string of IP addresses into individual elements, storing them as a list in the ip\_addresses variable. This allows for easier iteration in the next steps.

\# Use .split() to convert \`ip\_addresses\` from a string to a list  
ip\_addresses \= ip\_addresses.split()

\# Display the updated list  
print(ip\_addresses)

## Iterate through the remove list

In this task, I set up a for loop to iterate through the ip\_addresses list and display each element. This loop will be essential for removing any IP addresses that match those in the remove\_list.

\# Build iterative statement: loop through \`ip\_addresses\` to check against \`remove\_list\`  
for element in ip\_addresses:  
    print(element)

## Remove IP addresses that are on the remove list

The conditional statement checks whether each element of the ip\_addresses list is present in the remove\_list. If so, the .remove() method is used to remove that element from the ip\_addresses list. Since there are no duplicates in the list, using .remove() works effectively without errors.

\# Conditional statement: If current element is in \`remove\_list\`, remove it from \`ip\_addresses\`  
for element in ip\_addresses:  
    if element in remove\_list:  
        ip\_addresses.remove(element)

\# Display updated list  
print(ip\_addresses)

## Update the file with the revised list of IP addresses 

I used the .join() method to convert the updated ip\_addresses list back into a string, separating each IP address by a new line. Then, using the open() function in write mode ("w"), I replaced the old contents of the file with the revised list.  
\# Convert the list back to a string with new line separators  
ip\_addresses \= "\\n".join(ip\_addresses)

\# Write the updated list back into the file  
with open(import\_file, "w") as file:  
    file.write(ip\_addresses)

Finally, I verified that the file was successfully updated by reading its contents again and displaying the result.

\# Verify the contents of the updated file by reading it  
with open(import\_file, "r") as file:  
    text \= file.read()

\# Display the updated contents  
print(text)

## Summary

In this project, I created an algorithm to automate the process of removing specific IP addresses from an allow list based on a remove list. The key components of the algorithm include opening and reading the file, splitting the contents into a list, iterating through the list to find and remove specific IP addresses, and finally updating the file with the revised list. This solution provides an efficient way to maintain access control lists for sensitive information using Python's file handling and list manipulation features.  
