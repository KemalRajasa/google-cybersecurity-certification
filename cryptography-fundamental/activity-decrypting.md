In this scenario, all of the files in your home directory have been encrypted. You’ll need to use Linux commands to break the Caesar cipher and decrypt the files so that you can read the hidden messages they contain.

Here’s how you’ll do this task: First, you’ll explore the contents of the home directory and read the contents of a file. Next, you’ll find a hidden file and decrypt the Caesar cipher it contains. Finally, you’ll decrypt the encrypted data file to recover your data and reveal the hidden message

Two files, Q1.encrypted and README.txt, and a subdirectory, caesar, are listed:

`Q1.encrypted  README.txt caesar`

Use the ls -a command to list all files, including hidden files, in your home directory.
This will display the following output:

`.  ..  .leftShift3`

Use the cat command to list the contents of the .leftShift3 file.

`cat .leftShift3 | tr "d-za-cD-ZA-C" "a-zA-Z"`

and wil return output:

`openssl aes-256-cbc -pbkdf2 -a -d -in Q1.encrypted -out Q1.recovered -k ettubrute`

command breakdown: In this instance, the openssl command reverses the encryption of the file with a secure symmetric cipher, as indicated by AES-256-CBC. The -pbkdf2 option is used to add extra security to the key, and -a indicates the desired encoding for the output. The -d indicates decrypting, while -in specifies the input file and -out specifies the output file. The -k specifies the password, which in this example is ettubrute.
