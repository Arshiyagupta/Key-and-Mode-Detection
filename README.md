# Key-and-mode-detection

In this jupyter notebook, a key finding method has been written.
Data set used is called GTZAN. This is available at 

http://marsyas.info/downloads/datasets.html

Key annotation to each song in this data set is attached in this github folder as "keys" 

To run the code, please download following dependencies
numpy
scipy
librosa
pandas
util (this .py file is attached in this github folder)

Steps to finding key, as present in jupyter notebook
1. Audio files are loaded using librosa.

2. Chroma vector is extracted for each song, using librosa. Each vector is an array of shape (12,1)

3. Function is downloaded from following URL 

https://gist.github.com/bmcfee/1f66825cef2eb34c839b42dddbad49fd

for comparing chroma vector with Krumhansl-Schmuckler's chroma templates.

4. This returns a dot product of song chroma with all 24 templates. Highest value is chosen and declared as predicted key.

5. Actual keys are uploaded into jupyter notebook. The file is present in the current github folder.

6. Comparison between actual and prediced keys are made using function from this URl

https://github.com/craffel/mir_eval/blob/master/mir_eval/key.py"""

This attributes 100% score for correct estimation of key and mode
50% score for estimating a key major 5th above the actual key
25% score for estimating a relative major/minor of actual key
20% score for estimating a parallel major/minor of actual key

Accuracy of current model is 40%.
