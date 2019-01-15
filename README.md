# pc_member_compare
This simple script compares the Program Committee members of two venues

# Usage
Add execution right to the script
```
$ chmod +x compare_tcp.sh
```

## How to use
Example: `./compare_tcp.sh <input_file1> <input_file2>`

```
Input files are plain text files, each line containing the name of a PC member

<input_file1> is the conference you are aiming at, i.e., comparison and percentage information will be calculated accordingly!

The intersection (if there is any) will be printed out to <input_file1___VS___input_file2> as well as to `STDOUT`
Ensure your input files contain only the name and nothing more!
```
# Example
See some example TPC list in the repository and compare them!
```
./compare.sh asiaccs_2019 ccs_2018
```
## Output
```
Cleaning up...[DONE]
Reading input file asiaccs_2019 and comparing to input file ccs_2018
Match logged:  Adam Doupé 
Match logged:  Cas Cremers 
Match logged:  Debin Gao 
Match logged:  Giancarlo Pellegrino 
Match logged:  Gianluca Stringhini 
Match logged:  Hao Chen 
Match logged:  Heng Yin 
Match logged:  Kai Chen 
Match logged:  Kehuan Zhang 
Match logged:  Long Lu 
Match logged:  Lorenzo Cavallaro 
Match logged:  Lucas Davi 
Match logged:  Neil Gong 
Match logged:  Ninghui Li 
Match logged:  Tibor Jager 
Match logged:  Ting Yu 
Match logged:  Yang Liu 
Match logged:  Yinqian Zhang 
Match logged:  Yongdae Kim 
Match logged:  Yuan Tian 
We have found 20 matching TPC members in the inersection of asiaccs_2019 and ccs_2018


20.6186% of asiaccs_2019 has been a TPC in ccs_2018
[DONE]
```
This means that if your paper from CCS 2018 has been rejected and you are considering resubmitting to the lower-ranked AsiaCCS conference, you might end up having the same reviewers, or at least someone might recognize your paper as a resubmitted one. 

# What this application does not do for you
Preparing the text files with the names is your task.
The easiest way is the following:
 - Copy the list (usually with the affiliations that need to be omitted) from the website.
 - Open a sheet application (e.g., libreoffice calc, MS office excel, google sheets)
 - Right click and Paste special
 - Select the separator to 'Space', 'comma', 'Tab' depending on the source you have copied the list from
 - Cut out all new columns except the first one where you have clicked to paste the clipboard
 - Save to .csv

Of course, there are several other ways to do that (e.g., run your own crawler script :))
