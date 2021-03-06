niftijio
========

This project is a Java library for reading and writing NIfTI image
volumes.  This includes support for header metadata, various datatypes, and
multichannel volumes.  When a volume is read from a file, the image intensities
are stored in a four-dimensional double array.  The array indices match the
order in the 'dim' array of the header.

A jar can be built using Apache Ant by executing 'ant' in the project
directory.  An example main class is included and the jar will execute it when
run with the '-jar' option.  The following example will print the volume
dimensions and datatype to the console:

java -Xmx512M -jar niftijio.jar example.nii.gz

The file format specification can be found here:

http://nifti.nimh.nih.gov/nifti-1

The code for reading the header was derived from the following implementation:

http://niftilib.sourceforge.net

The code for little-endian streams is provided by Roedy Green:

http://mindprod.com/jgloss/endian.html

This is released under the MIT license.  Any comments can be directed to
cabeen@gmail.com
