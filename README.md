# Password-Checker
An API based password checker that runs on your local machine to check if your password was ever hacked.
In this project we use the `haveibeenpwned` api to check if a password that we are using has been hacked or not. 
The features of this project can also be used on the website `https://haveibeenpwned.com`. However, most of the time, even though the website is trusted and it uses https, we should never really trust a website with our password. Maybe a big website like facebook, google or something like that we trust. But ideally, we don't want to send our password over the internet. Because, as soon as we click pwned on the search bar, the password is being transferred to a server somewhere in the world, and somebody could actually intercept it. So, there is actually a more secure way of doing this. And this is what we are going to build. The same website gives us a password API for us to do the same thing that it does to check our password in a more secured way because we could trust the website, but the best security is to trust no-one.

## How does it work?
1. The user will enter their password which will be first SHA1 hashed.
2. The first 5 characters of the hashed password will be sent through the API to retrieve all the hashed passwords that match the first 5 characters of our hashed password
3. Upon receiving the list of passwords, along with the number of times they have been leaked, we will match that with our password to check if it was every hacked/leaked.

## How to use it?
This repository has an `.ipnyb` file which shows the whole creation of the project along with explanation at every step. At the end of the file there are two blocks of codes - 
1. The second last block of code can be ran on the Python IDE user decides to use.
2. The last block of code can only be used on terminal. To run it on terminal follow the following steps - 
    - Copy the last block of code and store it in a Python file with an extension of `.py`
    - Open the command prompt/terminal on your system
    - Set the working directory on your terminal to be the same as that of the `.py` file of the password checker
    - Type the following command - `python3 <filename.py> <yourpassword>`

## Future Scope - 
When we run a script on terminal, and press the up arrow we can see the previous commands we ran. So, that means that the password we entered to check if it has been hacked or not is still stored somewhere on our system. To make it more private, since this whole project is about privacy, we can read the passwords from a text file instead of tying it out in the terminal.
