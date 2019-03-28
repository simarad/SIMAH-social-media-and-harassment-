# SIMAH-social-media-and-harassment- evaluation script

This is the official evaluation script for SIMAH(social media and harassment). This script is prepared for both task A and B.


NOTE During the Practice phase, the prediction files submitted by participants to the task page will be evaluated for the task A, and for demonstration purposes only; if participants wish to test the script on prediction files for task B as well, they could use the version available here (see the instructions at the bottom of this page).



Submission instructions

The script takes one single prediction file as input, that MUST be a TSV file structured as follows:

Task A

id[tab]{0|1}

e.g.

101[tab]1
102[tab]0
103[tab]1

Task B

id[tab]{0|1}[tab]{0|1}[tab]{0|1}

e.g.

101[tab]1[tab]1[tab]1
102[tab]0[tab]0[tab]0
103[tab]1[tab]1[tab]0
104[tab]1[tab]0[tab]0
105[tab]1[tab]0[tab]1

File names

When submitting predictions to the task page in Codalab, one single file should be uploaded for each task, as a zip-compressed file, and it should be named according to the task predictions are submitted for, therefore:

en_a.tsv for predictions for taskA-English
en_b.tsv for predictions for taskB-English

Submission results

The script outputs a file scorer.txt containing different scores. For task A and B it returns accuracy, precision, recall and F1-score just for the harassment category. For task B it returns accuracy, precision, recall and F1-score for each category (Indirect harassment, physical harassment, sexual harassment), along with the macro-averaged F1-score. 

Testing the script offline

In order to run the script locally, the input and output directories must match the Codalab format. The input directory must contain two subdirectories, namely res (containing the result file in TSV format with the naming convention described above) and ref containing the reference dataset (called en.tsv for English and es.tsv for Spanish). The output will be written in the file scorer.txt in the output directory. Example of file structure:

input/
 |- ref/
     |- en.tsv
 |- res/
     |- en_a.tsv
output/
 |- scorer.txt
