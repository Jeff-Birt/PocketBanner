# PocketBanner
Banner printing on Casio FX-820P (data compression in BASIC)

I thought it would be fun to create a banner printing program for the Casio FX-820P, a 1980s pocket computer with a built-in printer. With only 3.6K of RAM available using a simple bitmap for 26, 20*5, characters would consume most of the RAM.

DATA “1234567”,”1234567”,”123456”

4 bytes		One blank DATA statement

20 bytes	Bitmap characters

8 bytes		Quotes and commas

= 32 bytes	Per line

32 x 5 x 26 = 4,160 bytes – oops too large

To save RAM we use a simple data compression method called Run Length Encoding (RLE). This saves RAM but makes the program more complicated as we have to decode the RLE. There are REM statements which explain how it works. 

Files:
Banner Program 5 Raw Data.txt – basic RLE, easier to understand
Banner Program 5.txt – further optimized to save more RAM
