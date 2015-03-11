# Repairing URL's from the Report Designer HTM/HTML output
    This script repairs the erroneous <a> tag's created by the Report Designer, if hyperlinks are enabled.

    If you're creating a report and saving it as an HTM or HTML file, the <a> tags will look like this:
        <a href="True"><nobr>http://www.esri.com/</nobr></a></span>

    This creates a hyperlink using the URL, but that link leads to a non-existent file call "True".

    This script will repair those links, and remove the redacted <nobr> tags, making the URL's function correctly.

    Occasionally the user will want to make a Table of Contents HTM file in conjunction with the report. This script will detect that TOC file as long as it has the same name as the report HTM file, and update the links in that TOC file to utilize the repaired HTML file.

## Caveat
* This script requires the Beautiful Soup 4 module, found here:
        http://www.crummy.com/software/BeautifulSoup/#Download
  From that zip file, move the "bs4" folder into the following directory:
        C:\Python27\ArcGIS10.x\Lib\site-packages
* This script could potentially run just fine with any HTM file, so verify that you are using it to correct HTM or HTML files created with the Report Designer.

## How can I run this?
This runs as a standalone script in any Python IDE, using Python 2 from Esri.

## Unfamiliar with Python?
* The following is a blog article that documents some ways for you to familiazrize yourself with python -
[Seven easy ways to start learning Python and ArcPy](http://blogs.esri.com/esri/supportcenter/2014/03/26/8-easy-ways-learning-python-arcpy/)