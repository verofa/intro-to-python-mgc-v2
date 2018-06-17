# Introduction to Python Version 2
## Creating an application to send and receive secret messages

In this project, you will learn how to make your own encryption program using Python (that is an interpreted high-level programming language for general-purpose programming) to send and receive secret messages with a friend. 

In this project you will also learn programming concepts as:

- Iteration (looping) over a string variable;
- The find() method;
- The modulus operator (%).
- **for** loops;

## Prerequisites

Before get on with it to successfully complete this tutorial in a Microsoft Windows Operating System, you must do the following:

1.- Download and install the [Visual Studio Code](https://go.microsoft.com/fwlink/?LinkID=534107) for Windows.

2.- Install a version of Python 3 (for which this tutorial is written), download from [python.org](https://www.python.org/ftp/python/3.6.5/python-3.6.5.exe)

3.- Install the extension from the [VS Code marketplace](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

4.- Make sure the location of your Python interpreter is included in your **PATH** environment variable. You can check this by running **path** at the command prompt. If the Python interpreter's folder is not included, open Windows Settings, search for "environment", select Edit environment variables for your account, then edit the Path variable to include that folder (C:\Program Files (x86)\Python36-32).
	
## Time to start coding!

### Step 1 - Understanding the Caesar cipher method or algorithm for performing encryption or decryption of a message.

The Caesar cipher is one of the oldest and simplest forms of encrypting a message, and its name come from Julius Caesar that was popular leader of the Roman Republic. 

A cipher is a type of secret code, where each letter in the original message (called the plaintext) is replaced with a letter corresponding to a certain number of letters shifted up or down (key) in the alphabet.

### Step 2 - Encrypting letters.

Let’s start by encrypting the letter **'E'** using a left shift of 3 as the key (but you can use any number you like), so that (for example) each occurrence of **E** in the plaintext becomes **B**.


![Caesar Cipher](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Caesar_cipher_left_shift_of_3.svg/640px-Caesar_cipher_left_shift_of_3.svg.png)

### Step 3 - Encrypting letters using Python.

Create a file in Visual Studio Code, name it 'main.py' and write it out as an alphabet variable.

![alphabet-variable](https://raw.githubusercontent.com/verofa/intro-to-python-mgc-v2/master/alphabet.PNG)

Keep in mind that each letter of the alphabet has a position, starting at position 0. So the letter ‘a’ is at position 0 of the alphabet, ‘b’ is at position 1, ‘c’ is at position 2 and so on.

![alphabet-number-position](https://codeclubprojects.org/en-GB/python/secret-messages/images/messages-array.png)


