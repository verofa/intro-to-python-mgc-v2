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

Let's see how we can get a specific letter from your variable **alphabet**, for example, if you want to "extract" the letter 'c' write below the declaration of the alphabet variable the following code :

```python
print(alphabet[2])
```

It should look more or less like this:

![Printing-letter-c](https://raw.githubusercontent.com/verofa/intro-to-python-mgc-v2/master/Printing-letter-c.PNG)

Now it is time to know what those two lines are doing. It is simple to run 'main.py' with Python. Right-click in the editor and select **Run Python File in Terminal** (which saves the file automatically ;) ):

![Executing-Code-VSC](https://raw.githubusercontent.com/verofa/intro-to-python-mgc-v2/master/Executing-Code-VSC.gif)

Add the following lines to your code:

```python
print(alphabet[8])
print(alphabet[0])
print(alphabet[14])
```

What is it the output? (You can delete the print statements once you have tried this out)

At this point you have learned how to work with an array (the values that store the variable **alphabet**) and extract the value that you want to use from it. Therefore, the next step to encrypt your message is to choose and configure the key you will need to encrypt your messages. For doing that, you will need to store the secret key in a variable as well:

```python
alphabet='abcdefghijklmnopqrstuvwxyz'
key = 3
```

Now you are ready to make your first program to encrypt a letter, adding the following lines to your code.

This line, is to ask to the person that is using the program (called **user**) to enter a character (single letter):
```python 
character = input('Please enter a character: ')
```

Then you have to calculate the position of that character, using the method **find** and then you are going to print it in the screen to know its value as shown bellow:

```python
position = alphabet.find(character)
print(position)
```

In the following example, the user is entering the character 'e' and the program is showing the position 4 as a result of the execution of it :

![Encrypting-character](https://raw.githubusercontent.com/verofa/intro-to-python-mgc-v2/master/Encrypting-character.gif)

Now that you know the position of the original character (letter) to encrypt it, you should add the **key** (remember its value is 3) to that position creating a new variable (**newPosition**) to store the position of the encrypted character.

```python
newPosition = position + key
```

![Encrypting-character-np](https://raw.githubusercontent.com/verofa/intro-to-python-mgc-v2/master/Encrypting-character-np.gif)
