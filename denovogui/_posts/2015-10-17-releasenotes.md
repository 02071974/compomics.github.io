---
name: ReleaseNotes
project: denovogui
layout: default
permalink: /denovogui/wiki/releasenotes.html
github_project: https://github.com/compomics/denovogui
---

# ReleaseNotes

---

**Changes in DeNovoGUI 1.7.13 (October 17. 2015):**

 * BUG FIX: The tag matches and BLAST exports now works again for Novor.

 * LIBRARY UPDATE: Updated utilities to version 4.1.2.

---

**Changes in DeNovoGUI 1.7.12 (October 15. 2015):**

 * BUG FIX: The peptide matches export now works again for Novor.
 * BUG FIX: Fixed a bug where the PTM mappings for the de novo algorithms where not saved correctly in the search parameters.

---

**Changes in DeNovoGUI 1.7.11 (October 14. 2015):**

 * FEATURE IMPROVEMENT: Extended the user selected file methods to support suggested/default file names.

 * LIBRARY UPDATE: Updated utilities to version 4.0.15.

---

**Changes in DeNovoGUI 1.7.10 (October 12. 2015):**

 * FEATURE IMPROVEMENT: Tags that are too short are now ignored in the peptide to protein mapping export.

 * LIBRARY UPDATE: Updated utilities to version 4.0.14.

---

**Changes in DeNovoGUI 1.7.9 (October 8. 2015):**

 * FEATURE IMPROVEMENT: Updated Novor to version v1.03.0489, fixing potential issues related to high resolution data with very low fragment ion tolerance.

---

**Changes in DeNovoGUI 1.7.8 (October 3. 2015):**

 * BUG FIX: Fixed a bug related to PTMs not targeting specific amino acids when setting up pNovo jobs.

 * LIBRARY UPDATE: Updated utilities to version 4.0.13.

---

**Changes in DeNovoGUI 1.7.7 (October 1. 2015):**

 * FEATURE IMPROVEMENT: Improved how some of the dialogs resize in low screen resolution conditions.

 * LIBRARY UPDATE: Updated utilities to version 4.0.11.

---

**Changes in DeNovoGUI 1.7.6 (October 1. 2015):**

 * BUG FIX: Corrected a typo on the sequencing handler resulting in a null pointer.

 * LIBRARY UPDATE: Updated utilities to version 4.0.10.

---

**Changes in DeNovoGUI 1.7.5 (September 26. 2015):**

 * FEATURE IMPROVEMENT: One algorithm is now run at a time and the duration of each is reported. 

---

**Changes in DeNovoGUI 1.7.4 (September 23. 2015):**

 * FEATURE IMPROVEMENT: Updated Novor to version 1.03.0479, adding support for setting the fragmentation type and mass analyzer.

 * BUG FIX: The peptide matches export now works again.

 * LIBRARY UPDATE: Updated utilities to version 4.0.8.

---

**Changes in DeNovoGUI 1.7.3 (September 21. 2015):**

 * NEW FEATURE: Added support for residue specific alpha values in the spectrum annotations, and used this to indicate the amino acid scores for Novor.

 * BUG FIX: Fixed a bug in the search feature which only searched the PepNovo results.

 * LIBRARY UPDATE: Updated utilities to version 4.0.6.

---

**Changes in DeNovoGUI 1.7.2 (September 14. 2015):**

 * FEATURE IMPROVEMENT: Updated Novor to version 1.01.0446, fixing an issue with reading some non-standard mgf files.

 * BUG FIX: Fixed a bug in the show all peaks option in the spectrum menu.
 * BUG FIX: Made sure that the Results Dialog is only opened if the sequencing actually generated any result files.

---

**Changes in DeNovoGUI 1.7.1 (September 12. 2015):**

 * BUG FIX: Novor fragment ion tolerances in ppm are now converted to Dalton in the backend (as ppm is not yet supported).

 * LIBRARY UPDATE: Updated jsparklines to version 1.0.6.
 * LIBRARY UPDATE: Updated utilities to version 4.0.5.

---

**Changes in DeNovoGUI 1.7.0 (September 3. 2015):**

 * NEW FEATURE: Added support for Novor.

 * FEATURE IMPROVEMENT: Added path settings option to the GUI.

 * BUG FIX: Fixed an issue with the wrapper in handling memory warnings for 32 bit Java 8.

 * LIBRARY UPDATE: Updated utilities to version 4.0.4.

---

**Changes in DeNovoGUI 1.6.0 (August 27. 2015):**

 * NEW FEATURE: PTM masses are now set via the atomic composition.
 * NEW FEATURE: The settings files are now called .par instead of .parameter.

 * FEATURE IMPROVEMENT: Improved the parsing of modifications from DirecTag output, such that PTMs targeting more than one residue can be parsed.

 * BUG FIX: Fixed a bug that made is impossible to swap between spectrum files in the Results frame.
 * BUG FIX: Fixed bugs in PathSettingsCLI where the paths could not be set.
 * BUG FIX: Corrected the handling of terminal PTMs for DirecTag. 
 * BUG FIX: Corrected a bug in the peptide mapping.
 * BUG FIX: Fixed bugs in the exports where pNovo+ was not added correctly. 
 * BUG FIX: Fixed an issue in the "More than one amino acid can be targeted by the modification X" warning where the name of the PTM was not shown.

 * LIBRARY UPDATE: Updated utilities to version 4.0.0.

---

**Changes in DeNovoGUI 1.5.2 (July 14. 2015):**

  * FEATURE IMPROVEMENT: Made it possible to open pNovo+ files via the Open menu item.
  * FEATURE IMPROVEMENT: Added a message that PepNovo+ does not have any advanced settings.

  * BUG FIX: Fixed bugs in the Tag Matches and BLAST exports.
  * BUG FIX: Fixed a bug in the loading of the results which slowed down the loading process.
  * BUG FIX: Fixed a bug in the sorting of the columns.

  * LIBRARY UPDATE: Updated utilities to version 3.49.23.


---


**Changes in DeNovoGUI 1.5.1 (July 6. 2015):**

  * FEATURE IMPROVEMENT: Redesigned the settings dialog to work better on smaller screens.
  * FEATURE IMPROVEMENT: Improved the way the advanced de novo parameters are set.

  * LIBRARY UPDATE: Updated utilities to version 3.49.22.


---


**Changes in DeNovoGUI 1.5.0 (June 19. 2015):**

  * NEW FEATURE: Added support for pNovo+ (beta).
  * NEW FEATURE: Added support for mirrored spectra in the results frame.

  * FEATURE IMPROVEMENT: Mass tolerances can now be provided in ppm.
  * FEATURE IMPROVEMENT: Improved the color coding for the ID column in the Results frame.
  * FEATURE IMPROVEMENT: Updated the "please cite us" link in the tip of the day to include the real link to the paper.
  * FEATURE IMPROVEMENT: Added a check for if DeNovoGUI is started from within a zip file.
  * FEATURE IMPROVEMENT: Increased the size of the spectrum panel.
  * FEATURE IMPROVEMENT: Made it possible to set the Java Home from the GUI.
  * FEATURE IMPROVEMENT: Improvements to the handling of errors on the command line.
  * FEATURE IMPROVEMENT: Added a new simpler way of resetting the spectrum annotation.

  * BUG FIX: Fixed a bug in the progress counter for PepNovo+.
  * BUG FIX: Fixed JavaDoc errors so that it builds again in Java 8.
  * BUG FIX: Fixed an issue in the annotation preferences that occurred if no identifications were found.

  * LIBRARY UPDATE: Updated utilities to version 3.49.11.


---


**Changes in DeNovoGUI 1.4.12 (October 23. 2014):**

  * FEATURE IMPROVEMENT: PTM tooltips now include "confident" or "not confident" in addition to the color coding.
  * FEATURE IMPROVEMENT: Renamed "no enzyme" to the more understandable "unspecific".

  * BUG FIX: Fixed issues with using search parameter settings files from SearchGUI.

  * LIBRARY UPDATE: Updated utilities to version 3.40.0.


---


**Changes in DeNovoGUI 1.4.11 (September 17. 2014):**

  * FEATURE IMPROVEMENT: Fixed an issue with indexing mgf files with empty charge tags.

  * LIBRARY UPDATE: Updated utilities to version 3.37.3.


---


**Changes in DeNovoGUI 1.4.10 (September 12. 2014):**

  * BUG FIX: Fixed more bugs where the export of peptide matches was broken.


---


**Changes in DeNovoGUI 1.4.9 (September 11. 2014):**

  * BUG FIX: Fixed a bug where the export of peptide matches was broken.

  * LIBRARY UPDATE: Updated jsparklines to version 1.0.4.
  * LIBRARY UPDATE: Updated utilities to version 3.37.1.


---


**Changes in DeNovoGUI 1.4.8 (August 29. 2014):**

  * NEW FEATURE: Added "type to find" in the PTM table in the Search Settings dialog.
  * NEW FEATURE: Added PTM tooltips in the Search Settings dialog.

  * BUG FIX: Fixed a bug in the use of custom PTM patterns.

  * LIBRARY UPDATE: Updated utilities to version 3.35.5.


---


**Changes in DeNovoGUI 1.4.7 (August 27. 2014):**

  * BUG FIX: Fixed a bug that stopped DeNovoGUI if only DirecTag was used.


---


**Changes in DeNovoGUI 1.4.6 (August 21. 2014):**

  * BUG FIX: Fixed an issue in the auto update feature that could occur on specific client machine setups.

  * LIBRARY UPDATE: Updated utilities to version 3.35.3.


---


**Changes in DeNovoGUI 1.4.5 (August 8. 2014):**

  * BUG FIX: Fixed a bug in the spectrum annotation of tags.

  * LIBRARY UPDATE: Updated utilities to version 3.31.2.


---


**Changes in DeNovoGUI 1.4.4 (July 31. 2014):**

  * FEATURE IMPROVEMENT: Improved the tag to protein mapping.

  * LIBRARY UPDATE: Updated utilities to version 3.30.1.


---


**Changes in DeNovoGUI 1.4.3 (July 29. 2014):**

  * NEW FEATURE: Added indicators of the supported platforms for each search engine.

  * FEATURE IMPROVEMENT: Added the TIC cut-off in the DirecTag command line.
  * FEATURE IMPROVEMENT: Made sure that closing a dialog is always considered the same as using the cancel button.

  * LIBRARY UPDATE: Updated jsparklines to version 0.8.0.
  * LIBRARY UPDATE: Updated utilities to version 3.29.7.


---


**Changes in DeNovoGUI 1.4.2 (June 25. 2014):**

  * FEATURE IMPROVEMENT: If there is no internet connection the check for new version no longer prints an error log to the log file.
  * FEATURE IMPROVEMENT: Improved the speed of the Waiting Dialog.
  * FEATURE IMPROVEMENT: Cleaned up the closing of internal database connection.

  * LIBRARY UPDATE: Updated utilities to version 3.28.30.


---


**Changes in DeNovoGUI 1.4.1 (May 19. 2014):**

  * FEATURE IMPROVEMENT: Updated the Java Settings dialogs.

  * BUG FIX: Fixed a bug in the Peptide Matches export where the database connection was dropped.

  * LIBRARY UPDATE: Updated utilities to version 3.26.38.


---


**Changes in DeNovoGUI 1.4.0 (April 30. 2014):**

  * NEW FEATURE: Added Linux support for DirecTag (32 and 64 bit).
  * NEW FEATURE: Added 32 bit and 64 bit versions of DirecTag for Windows.
  * NEW FEATURE: DirecTag is now disabled on Mac (as a Mac build is not yet available).
  * NEW FEATURE: PepNovo is now disabled on Linux 32 bit (as a 32 bit build is not available).
  * NEW FEATURE: Added new command line options for path configuration.

  * FEATURE IMPROVEMENT: Added the possibility for the user to turn the auto update on and off.
  * FEATURE IMPROVEMENT: The Bug Report dialog now refers to the DeNovoGUI Google Group.

  * BUG FIX: Fixed a typo in the reference to the CLI wiki page.
  * BUG FIX: Fixed a bug in the Job class where the process was always referred to as PepNovo.
  * BUG FIX: Fixed a bug in the algorithm location dialog where the browse button for DirecTag referred incorrectly to PepNovo.
  * BUG FIX: If either the PepNovo or DirecTag commands fails the whole process is now canceled. (Instead of opening empty results as before.)

  * LIBRARY UPDATE: Updated utilities to version 3.26.28.


---


**Changes in DeNovoGUI 1.3.7 (April 10. 2014):**

  * NEW FEATURE: The DeNovoGUI report is now saved in the output folder.

  * BUG FIX: Fixed a bug in the peptide matches export filters.


---


**Changes in DeNovoGUI 1.3.6 (April 8. 2014):**

  * FEATURE IMPROVEMENT: Added score and number of matches filter for all export options.


---


**Changes in DeNovoGUI 1.3.5 (April 3. 2014):**

  * BUG FIX: Enabled the export for DirecTag results.
  * BUG FIX: Fixed an issue with the creation of terminal PTMs without specific targets.

  * LIBRARY UPDATE: Updated utilities to version 3.26.9.


---


**Changes in DeNovoGUI 1.3.4 (April 1. 2014):**

  * FEATURE IMPROVEMENT: Implemented memory setting and restart by the user.
  * FEATURE IMPROVEMENT: Added catching of the out of memory error when mapping to FASTA file.

  * BUG FIX: Fixed a bug in the protein iterator where the last protein was not included.

  * LIBRARY UPDATE: Updated utilities to version 3.26.4.


---


**Changes in DeNovoGUI 1.3.3 (March 30. 2014):**

  * BUG FIX: Fixed a bug that made it impossible to load DirecTag results without at least one fixed modification in the settings.

  * LIBRARY UPDATE: Updated utilities to version 3.26.3.


---


**Changes in DeNovoGUI 1.3.2 (March 27. 2014):**

  * BUG FIX: Fixed a bug where results from both algorithms was tried loaded at the end of the processing even if only one algorithm was used.


---


**Changes in DeNovoGUI 1.3.1 (March 27. 2014):**

  * BUG FIX: Fixed a bug in the method for getting all non fixed modifications, used in the export peptides feature.

  * LIBRARY UPDATE: Updated utilities to version 3.25.14.


---


**Changes in DeNovoGUI 1.3.0 (March 26. 2014):**

  * NEW FEATURE: Added support for DirecTag.
  * NEW FEATURE: Added tags to FASTA file mapping. (beta)
  * NEW FEATURE: Added the possibility to create identification parameters files from the command line.
  * NEW FEATURE: Added the option of setting the maximum number of hits to export per spectrum for the BLAST export.

  * FEATURE IMPROVEMENT: Improved the memory handling of the object cache.
  * FEATURE IMPROVEMENT: Updated the TMT modifications to support 10-plex.
  * FEATURE IMPROVEMENT: Extended the export.
  * FEATURE IMPROVEMENT: Added the high resolution annotation option to the spectrum menu.

  * BUG FIX: Fixed a bug in the settings dialog that closed the settings dialog if the user canceled the save as dialog.

  * LIBRARY UPDATE: Updated utilities to version 3.25.12.


---


**Changes in DeNovoGUI 1.2.3 (November 27. 2013):**

  * FEATURE IMPROVEMENT: Improved the information printed to the waiting dialog during the sequencing.
  * FEATURE IMPROVEMENT: The possible mass deltas for the manual de novo sequencing are now set in correspondence with the PTMs used for the sequencing.
  * FEATURE IMPROVEMENT: Added tooltips with the maximum fragment ion and precursor mass tolerances to the Settings Dialog.
  * FEATURE IMPROVEMENT: The default PTMs selection in the Search Settings Dialog is now only shown if All Modifications is selected.
  * FEATURE IMPROVEMENT: Removed the Search Settings saving from the Settings Dialog.

  * BUG FIX: The PepNovo PTM mapping is now stored in the search parameters.
  * BUG FIX: Made sure that only valid search parameter files can be selected.
  * BUG FIX: Fixed GUI bugs in the progress dialogs when exporting to file.
  * BUG FIX: The exception handler now refers to DeNovoGUI web pages (and not PeptideShaker as before).

  * LIBRARY UPDATE: Updated utilities to version 3.18.10.


---


**Changes in DeNovoGUI 1.2.2 (October 8. 2013):**

  * BUG FIX: Fixed a bug where the startup log was always empty.
  * BUG FIX: Fixed a bug in the wrapper used to start the tool.

  * LIBRARY UPDATE: Updated utilities to version 3.15.23.


---


**Changes in DeNovoGUI 1.2.1 (October 5. 2013):**

  * BUG FIX: Fixed a bug in the reporter ion masses shown in the Modification Details dialog.

  * LIBRARY UPDATE: Updated utilities to version 3.15.20.


---


**Changes in DeNovoGUI 1.2.0 (September 27. 2013):**

  * NEW FEATURE: Added a "one-click BLAST" option to the De Novo Peptides table.
  * NEW FEATURE: Added BLAST compatible matches export.
  * NEW FEATURE: Added a spectrum annotation dialog to the results dialog where the user can select the annotation accuracy and level.
  * NEW FEATURE: Added an edit modifications edit option to the settings dialog.

  * FEATURE IMPROVEMENT: Added the spectrum details in front of every PSM in the default export.
  * FEATURE IMPROVEMENT: Updated the help text regarding the terminal mass gaps and how they affect the peak annotation.
  * FEATURE IMPROVEMENT: Hid the enzyme and model settings from the settings dialog.
  * FEATURE IMPROVEMENT: Added a new default precursor tolerance of 0.5 Dalton.
  * FEATURE IMPROVEMENT: Fixed terminal PTMs are now treated as variable PTMs.

  * BUG FIX: Reporter ions are now displayed in the spectrum annotation.
  * BUG FIX: The same fragment ion accuracy is now used in the manual and automatic de novo sequencing and peak annotation.
  * BUG FIX: Removed the spectrum help details referring to the plots that are not used.

  * LIBRARY UPDATE: Updated utilities to version 3.15.6.


---


**Changes in DeNovoGUI 1.1.0 (August 11. 2013):**

  * NEW FEATURE: Added a first version of a peptide sequence search feature in the results frame. (beta)

  * FEATURE IMPROVEMENT: Improved the way the N and C terminal gaps are shown in sequence column in the de novo matches table.
  * FEATURE IMPROVEMENT: Added the version number to the results frame title bar.
  * FEATURE IMPROVEMENT: Made sure that the results frame is shown in the middle of the screen if minimized.
  * FEATURE IMPROVEMENT: Added better error handling when re-loading de novo results and the wrong mgf file is selected.
  * FEATURE IMPROVEMENT: Fixed some issues with the size of the help dialogs.
  * FEATURE IMPROVEMENT: Added a progress dialog if the reference dataset has to be re-indexed.
  * FEATURE IMPROVEMENT: Fixed PTMs can now be shown in the GUI (both for the table and the spectrum).

  * BUG FIX: Terminal PTMs are now handled correctly.
  * BUG FIX: Fixed PTMs are now handled correctly.
  * BUG FIX: Added support for the N and C terminal gaps in the spectrum annotation.
  * BUG FIX: Set the correct max values for the spinners in the Settings dialog.
  * BUG FIX: The Settings dialog now resizes correctly.
  * BUG FIX: Fixed bugs in the peptide m/z values in the peptide table.

  * LIBRARY UPDATE: Updated utilities to version 3.14.21.


---


**Changes in DeNovoGUI 1.0.0 (July 16. 2013):**

  * The first public release of DeNovoGUI.


---