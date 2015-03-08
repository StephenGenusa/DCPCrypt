     =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
     =       DCPcrypt Cryptographic Component Library v2.1     =
     =                                                         =
     =          Copyright (c) 1999-2009 David Barton           =
     =                                                         =
     =         Further Changes by Henri Gourvest,              =
     =             Warren Postma and others                    =
     =           to support Delphi XE and up.                  =
     =                                                         =
     =   	warren.postma@gmail.com                        =
     =     https://bitbucket.org/wpostma/dcpcrypt2010          =
     =                                                         =
     =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=    

UPDATE JANUARY 2014:
 Updated and tested with Delphi 2009, 2010, XE, XE2, XE3, XE4, XE5
 by Warren Postma.  
  
 Please report bugs on Delphi versions XE or newer at bitbucket
 here: https://bitbucket.org/wpostma/dcpcrypt2010

Introduction:

DCPcrypt is a collection of cryptographic components for Delphi, 
and C++ Builder. Version 2.1 should work with almost all versions of
Delphi, from ancient versions like Delphi 5 to the latest versions as
of 2014, which is Delphi XE5. 

** The remainder of this introduction was written around 2003 and 
 has not been modified since then, and was written by David Barton. **

The idea behind DCPcrypt is that it should be possible to "drop in"
any algorithm implementation to replace another with minimum or no
code changes. To aid in this goal all cryptographic components are
descended from one of several base classes, TDCP_cipher for encryption
algorithms and TDCP_hash for message digest algorithms.

DCPcrypt is open source software (released under the MIT license) and
as such there is no charge for inclusion in other software. However, I
am currently a student and if you are making money from my software I
would really appreciate a donation of some sort, whether financial or
a license for the software you develop (or if anyone wants to sponsor 
a Mathematical Modelling (Masters) student for their final year...). 
Please note THIS IS NOT COMPULSORY IN ANY WAY. See 
http://www.cityinthesky.co.uk/cryptography.html for details on 
financial donations.

This software is OSI Certified Open Source Software.
OSI Certified is a certification mark of the Open Source Initiative.

If you maintain a website then a link to my page at 
http://www.cityinthesky.co.uk/ would be great!



What's New:

Changes since DCPcrypt v2 Beta 2 include

  *  Corrected C++ Builder compilation problem.


Changes since DCPcrypt v2 Beta 1 include

  *  Renamed source code files for hashes and ciphers to DCPxxx.pas
  
  *  Change the format of Cipher.InitStr so that the hash algorithm
     used to generate the key is explicitly specified. In order to
     get the same functionality as before, use TDCP_sha1.
     e.g. Cipher.InitStr('Hello World',TDCP_sha1);

  *  Block ciphers are now inherited from an intermediate component
     that implements the block size specific chaining mode encryption
     routines.

  *  Remove the internal component registration, it was more hassle
     than it was worth. If there is a demand for this to be put back
     then I might...     

  *  Added the full range of operation modes for Haval. By changing
     the defines at the top of DCPhaval.pas you can specify the
     number of passes and the output hash size.
     
  *  Added the Tiger hash algorithm (192bit digest).
  
  *  Changed the name of the file containing TDCP_ripemd160 for 
     consistency to DCPripemd160 from DCPrmd160.
     
  *  GOST no longer appears on the component palette pending verifying
     what the actual standard is (the code is still included however).

  *  Added the RipeMD-128 hash algorithm (128bit digest).
  
  *  Added the Serpent block cipher (AES finalist).
  
  *  Added the SHA-256,384,512 hash algorithms (256, 384, 512bit digest
     respectively).

  *  Added CTR chaining mode to all block ciphers.
  


Installation:

Delphi:      Open the appropriate package, DCPdelphiX.dpk where X is 
             your version of Delphi (either 4, 5 or 6). Then press the
             install button.

C++ Builder: Create a new design time package and add all the .pas
             files from the DCPcrypt2.zip archive including all those
             in the Ciphers and Hashes subdirectories. Then press the
             install button.

Kylix:       Open the DCPkylix.dpk package and then press the install
             button (note: Kylix 1 users may need to create a new
             package as with C++ Builder as this is a Kylix 2 package).

You may need to add the directory containing DCPcrypt (and the Ciphers
and Hashes subdirectories) to your library search path (found under 
Environment Options).

Once installed you will find two extra pages of components on your 
component palette, namely DCPciphers and DCPhashes. You can now place 
these components onto the form of your application to start using the 
algorithms.



Usage:

See the main html documentation in the Docs subdirectory.



Contact:

I appreciate knowing what DCPcrypt is being used for and also if you 
have any queries or bug reports please email me at crypto@cityinthesky.co.uk. 



DCPcrypt is copyrighted (c) 1999-2003 David Barton.
All trademarks are property of their respective owners.
