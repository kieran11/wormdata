# wormdata
THis repository has the worm data and the script to analyze the data.

The repository can be cloned, and the script can be run in RStudio without any changes to any part of the script. 

The .Rmd file has all the code to replicate the analysis. 

The four figures are here: wormdataanalysis_files/figure-gfm. They are four .png files. 
# steps and method

There are six replicates in the original Excel dataset. The first portion of the program takes the six replicates in the Excel file. It bind them together. 

It then creates a dataset with all of the unique combination from A to L.

This leaves us with 132 rows, or 144 - 12. There are 12 rows which are the diagonal products. 

Finally, we make two comparisons: 

1.  We use a t-test to compare the actual values (the diagonal elements) to the predicted values (the products of different elements) and determine whether we can reject the null that there is no difference between the diagonal products and the actual value. 
2.  We use a t-test to again compare the actual and predicted values. However, to determine whether we can reject the null, we adjust the p-value. We use the Benjamini & Hochberg (1995) adjustment. 

