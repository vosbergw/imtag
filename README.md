[imtag](http://github.com/vosbergw/imtag) is a frontend to the
 [pyexiv2](http://tilloy.net/dev/pyexiv2/) 
library that will let you 'set' or 'get' the Exif, Iptc and Xmp 
metadata.raw_value.

No validation of any sort is done! It is up to **you** to back up 
**your** images before making any changes!
If you can get the command line to accept your key/value and then 
if the [pyexiv2](http://tilloy.net/dev/pyexiv2/) 
library will accept it as a key/value pair, it will be set.

{% codeblock imtag command line help %}
$ ./imtag --help
usage: imtag [-h] [-e] [-i] [-x] [-g key.name | -s key.name=value] [-q] [-f]
             [-p] [--seperator SEP] [--escape]
             Files [Files ...]

Dump exif, iptc and xmp data from an image file.

positional arguments:
  Files              list of image file names to operate on

optional arguments:
  -h, --help         show this help message and exit
  -e, --exif         dump exif data (default is --exif --iptc --xmp)
  -i, --iptc         dump iptc data (default is --exif --iptc --xmp)
  -x, --xmp          dump xmp data (default is --exif --iptc --xmp)
  -g key.name        keys to list, can be specified multiple times
  -s key.name=value  Key/value pairs to modify. Can be specified multiple
                     times (will warn if operating on multiple files) Use
                     key.name=NULL to delete the entry. The string passed in
                     will be interpreted as a python object, so you may pass
                     list or dict objects as well as function calls
                     (=datetime.datetime(yy,mm,dd,hh,mm)
  -q, --quiet        don't display a warning about overwriting files
  -f, --force        force setting keys on multiple files
  -p, --prefix       prefix the filename to the output (useful with -g on
                     multiple files)
  --seperator SEP    seperator string (default=":")
  --escape           escape output - can be useful if you are trying to use
                     the output strings in a script
{% endcodeblock %}


