# repo_file_checker 

# Updated: 06. Jun. 2017

### The Repo File Checker functions:

  - creates a Report in a HTML format. Which will contains a list from the files and if there were any errors during the checking process then an error list.
  - with the phpMussel library (https://github.com/Maikuolan/phpMussel) it is checking the viruses, file extensions, contents.
  - comparing the MIME type and the extension
  - checking the ZIP files passwords.
  - checking the file names are valid or not? (contains spaces or special characters)
  - checking the file duplications
  - the phpMussel have a file extension Black and White list and also a file size limit option. Both of them is available in the phpMussel/vault/config file.

### Using:
  - add a temp Directory location to the config.ini file.
  - register and create an API key on the "Virus Total API" and add the API key to the phpMussel/vault/config.ini -> vt_public_api_key section
This is needed for the file virus checking.
  - call the index.php file from the CLI -> php -f .\index.php directory_what_i_want_to_check


### Test Files:
You can find the testFiles in the _testFiles folder. We have test for the following cases:
  - duplicates -> duplicated files
  - goodFiles -> every file is okay, html report will be generating
  - pwProtected -> there is a password protected zip file in the folder.
  - wrongContent -> here We removed the PDF text from the PDF file source. And we renamed the gif file to png.
  - wrongFilename -> the filename contains not legal characters
  - wrongMIME -> wrong MIME types


### Future developments:
  - checksum checker
  - copy files to staging area (Before the checks or after? Based on the config.ini location)
  - some kind of activity loader for the big size file checks.
  

