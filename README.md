# IE-Omics
iterative exclusion script for generating exclusion lists from previous runs

IEomics and III Manual: For users

# Step 1: Locate Necessary Programs
 *	R, use the version with this distribution:                                                                         IE_Omics_AND_III\R-3.3.3\bin\x64\Rgui.exe
 *	MSConvert (ProteoWizard), use the version with this distribution: IE_Omics_AND_III\msconvert64\MSConvertGUI.exe

IEomics:

# Step 2: File Conversion in MSConvert
* MS2 for R script
  * Upload .raw
  * Peak Picking (Vendor): Level: 2-2 (not Vendor for waters)
  * msLevel: 2-2
  * threshold: absolute .0001 most intense
  * Output: MS2

# Step 3: Run the script
 *	Open the code ([date]_IEomics.R) and after looking at the notes on the top of the script enter: Ctrl+Shift+S (or Ctrl+A and run), you can copy from a text editor and paste into R console. 
 *	A number of pop-up boxes will appear, read the dialogue box and enter the correct information. After the final pop-up box is entered a file will appear in the directory in which you imported the .ms2 files from. Note that pop-up boxes may appear behind all open windows, so minimize all open windows if pop-up boxes are not obvious. 

Step 4: Import exclusion list into the Thermo Methods File (for Thermo, other vendors methods vary)
 *	Import the generated exclusion list into the thermo methods file
 *	Change the exclusion tolerance to 100 ppm (recommended) or the exclusion tolerance desired
 *	Save the method file under a new name, and make sure to modify the sequence by adding the new method file
 *	Reinject the sample with the new ddMS2-topN Method with the imported exclusion list
 *	Repeat from Step 2. 
