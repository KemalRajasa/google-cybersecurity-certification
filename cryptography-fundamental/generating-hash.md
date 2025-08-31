Two files, file1.txt and file2.txt, are listed.

use cat to identify both file:

```

  analyst@4fb6d613b6b0:-$ cat file1.txt
  
  X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
  
  analyst@4fb6d613b6b0:-$ cat file2.txt
  
  X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*
  
```

it appears both file's content is identical, Although the contents of both files appear identical when you use the cat command, you need to generate the hash for each file to determine if the files are actually different.

Use the sha256sum command to generate the hash of the file.txt file and store it in a file called filehash

`sha256sum file1.txt >> file1hash`

`sha256sum file1.txt >> file1hash`

Use the cat command to display filehash

`cat file1hash`

`cat file2hash`

use the cmp command to highlight the differences

`cmp file1hash file2hash`

output will return:

`file1hash file2hash differ: char1, line 1`
