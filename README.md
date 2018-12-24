This is a fork of https://github.com/joeky888/youtube-xmL2ass with better color handling, which itself is a fork of https://github.com/nirbheek/youtube-ass with bug fixed

You can either convert a local XML file from youtube-dl to an .ass sub file, or download the XML from YouTube and convert that to an .ass sub file.

You'll need to install `requests` if you want to download the XML file from YouTube.

## Download the video's annotations as XML with youtube-dl
```sh
youtube-dl --write-annotations <VIDEO_URL>
```

## Download the video's annotations from YouTube and convert them
```sh
./youtube-xml2ass.py <VIDEO_ID>
```

The subs file will be named `<VIDEO_ID>.ass`.

## Convert the XML to ass subtitle
```sh
./youtube-xml2ass.py YOUR_XML_FILE.xml
```

The subs file will be named the same as your annotations file, but will remove `.annotations.xml` from the end and replace it with `.ass`.

Bugs fixed
======
* Python2/3 supported
* UTF-8 characters supported
* Using '16777215' as white color instead of '1'
* Escape '\n' in the  XML text area
* Format floating number to two decimal points
* Convert background colors from decimal RGB to BGR
* Use the opaque box BorderStyle to more closely mimic how annotations looked on YouTube (transparency would be nice as well, working on this)
* Can now download annotations XML from YouTube directly or process a local XML
