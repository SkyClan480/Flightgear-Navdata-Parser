# Flightgear-Navdata-Parser
Project by TOASTER and SkyClan480

To make use of this parser, you will need to have python installed. https://www.python.org/.

Download the correct excutable for your os. The file name says what os the executable is built for.

If you are on linux, you will need to make the file executable by running `chmod +x` on the file from the command line.

## How to use the parser:

1. Download [the latest NASR cycle](https://www.faa.gov/air_traffic/flight_info/aeronav/aero_data/NASR_Subscription/). You want either one listed under "Current" or "Preview". It will download as a .zip archive.
2. In the .zip there will be several text files. You will need to extract FIX.txt, NAV.txt, ILS.txt, and AWY.txt and put them in the same folder as the parser.
3. Run the parser. You will be prompted to enter the NASR effective date, which will be printed in the header of each file. The effective date of the data is listed on the website where you downloaded it. Enter the date into the prompt. This will create a folder called NavData.
5. Move the NavData folder wherever you want. In the FG launcher, you will need to alter some settings to make Flightgear use the new files. Under "addons", find "additional scenery folders" and add a new one. You'll want to add the folder that you put NavData in. For example, if you put NavData at C:\folder\fgstuff\NavData, you would add C:\folder\fgstuff as the scenery folder. Save this setting and then restart Flightgear for changes to take effect.

You can repeat this process for each new NASR cycle. Simply replace the old NavData folder with the new one. After the first time, you will not need to change flightgear settings in the future, as it will remember the directory and will automatically read the new files.

## Upcoming Changes
NASR nav script rework - Numerous changes to the NASR nav script to fix inconsistency problems involving NDB/DMEs, TACANs, VOR/DMEs, and VORTACs

ARINC 424 support - A separate set of scripts edited to parse from the ARINC 424 international format. These will be put on a separate version alongside the NASR version.

Procedures - Along with the ARINC 424 version will come departure and arrival procedure data. This functionality can't be added to the NASR version due to lack of necessary data.
