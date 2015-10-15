# Batch-combine-pdf-files

If you have a bunch of pdfs (e.g. like tables, figures, or manuscript as separate pdfs) and want to combine them into a single pdf for uploading to a journal:

First make sure you have ghostscript (check Program Files for "gs").
If you don't have it, download from http://www.ghostscript.com/download/gsdnld.html and run the .exe file.

In Notepad (or other text editor), put the following command:

```R
@echo off
"C:\Program Files\gs\gs9.06\bin\gswin64c.exe" -sDEVICE=pdfwrite -dNOPAUSE -dBATCH -dSAFER -sOutputFile="alltables.pdf" table_1.pdf table_2.pdf table_3.pdf table_4.pdf table_5.pdf table_6.pdf table_7.pdf
```

where "alltables.pdf" will be the output file, and table_1.pdf...is the list of your pdf files.

Save the text file as a .bat file in the directory that has the pdf files.  To do this in Notepad, save the file using " " marks:  "pdfcombine.bat"

Now, double click on the .bat file in Windows Explorer, and you should see your "alltables.pdf" file.
