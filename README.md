This is a fork of https://github.com/joeky888/youtube-xmL2ass with better color handling, which itself is a fork of https://github.com/nirbheek/youtube-ass with bug fixed

## Download the video's annotations as XML with youtube-dl
```sh
youtube-dl --write-annotations <VIDEO_URL>
```

## Convert the XML to ass subtitle
```sh
./youtube-xml2ass.py YOUR_XML_FILE.xml
```

Bugs fixed
======
* Python2/3 supported
* UTF-8 characters supported
* Using '16777215' as white color instead of '1'
* Escape '\n' in the  XML text area
* Format floating number to two decimal points
* Convert background colors from decimal RGB to BGR
* Use the opaque box BorderStyle to more closely mimic how annotations looked on YouTube (transparency would be nice as well, working on this)
