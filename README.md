# bash-assignment
Assignment 2: bash scripting exercise

### Question 1
How many processes are currently running on your system? Use ps and wc, the first line of output of ps is not a process!
```bash
ps -e | wc -l
```
__output__
```
236
```

### Question 2
Write a script that upon invocation shows the time and date, lists all logged-in users, and gives the system uptime. 
The script then saves this information to a logfile.

```bash
datetime= 'date'
users= 'who'
system='uptime'
  echo date and time: $datetime
  echo logged in users: $users
  echo system uptime: $system
```
__output__
```
Tue 26 Jul 2022 11:10:06 AM EAT
icipe    :0           2022-07-26 08:06 (:0)
date and time:
logged in users:
system uptime: uptime
```
### Question 3
Which command would you use in order to create an empty file in the current directory, let's say empty.txt?

```bash
touch empty.txt
```
__output__

```2014-01-31_JA-africa.tsv    201403160_01_text.json   bin          do         '[file]'    hello-world   jiy          mkdir       R                       snap
 2014-01-31_JA-america.tsv   33504-0.txt              date.sh      Documents   firstdir   jimmy         __MACOSX     Music       shell-lesson-data       Videos
 2014-01_JA.tsv              829-0.txt                Desktop      Downloads   for        Jimmy        'man ls'      pg514.txt   shell-lesson-data.zip
 2014-02-02_JA-britain.tsv   anaconda3                diary.html   empty.txt   gulliber   jimy          miniconda3   Pictures    shell-lesson.zip

2014-01-31_JA-africa.tsv    201403160_01_text.json   bin          do         '[file]'    hello-world   jiy          mkdir       R                       snap
 2014-01-31_JA-america.tsv   33504-0.txt              date.sh      Documents   firstdir   jimmy         __MACOSX     Music       shell-lesson-data       Videos
 2014-01_JA.tsv              829-0.txt                Desktop      Downloads   for        Jimmy        'man ls'      pg514.txt   shell-lesson-data.zip
 2014-02-02_JA-britain.tsv   anaconda3                diary.html   empty.txt   gulliber   jimy          miniconda3   Pictures    shell-lesson.zip
 ```

### Question 4
You are in /home/icipe/  suppose this directory is empty. How do you create in only one command the whole path /home/icipe/Work/mini-project/RNA-Seq/?

```bash
mkdir -p home/icipe/Work/mini-project/RNA-Seq/
```
__output__
```
 2014-01-31_JA-africa.tsv    date.sh     '[file]'       jiy          Pictures                trial-11.data   trial-1.data    trial-9.data
 2014-01-31_JA-america.tsv   Desktop      firstdir      less         R                       trial-12.data   trial-20.data  'universal greetings.txt'
 2014-01_JA.tsv              diary.html   for           __MACOSX     seq.txt                 trial-13.data   trial-2.data    universal_greetings.txt
 2014-02-02_JA-britain.tsv   do           gulliber     'man ls'      shell-lesson-data       trial-14.data   trial-3.data    Videos
 201403160_01_text.json      Documents    hello-world   miniconda3   shell-lesson-data.zip   trial-15.data   trial-4.data
 33504-0.txt                 Downloads    home          mkdir        shell-lesson.zip        trial-16.data   trial-5.data
 829-0.txt                   dt.sh        jimmy         Music        snap                    trial-17.data   trial-6.data
 anaconda3                   empty.txt    Jimmy         output.txt  'test.fa?raw=T'          trial-18.data   trial-7.data
 bin                         error.txt    jimy          pg514.txt    trial-10.data           trial-19.data   trial-8.data
```

### Question 5
Suppose your current working directory contains a file named seqs.txt. How do you rename this file into sequences.fasta? 
Does this have any effect on the content of the file, and if yes, what does it do?

```bash 
mv seq.txt sequence.fasta
```

__0utput__
```
 2014-01-31_JA-africa.tsv    date.sh     '[file]'       jiy          Pictures                trial-11.data   trial-1.data    trial-9.data
 2014-01-31_JA-america.tsv   Desktop      firstdir      less         R                       trial-12.data   trial-20.data  'universal greetings.txt'
 2014-01_JA.tsv              diary.html   for           __MACOSX     sequence.fasta          trial-13.data   trial-2.data    universal_greetings.txt
 2014-02-02_JA-britain.tsv   do           gulliber     'man ls'      shell-lesson-data       trial-14.data   trial-3.data    Videos
 201403160_01_text.json      Documents    hello-world   miniconda3   shell-lesson-data.zip   trial-15.data   trial-4.data
 33504-0.txt                 Downloads    home          mkdir        shell-lesson.zip        trial-16.data   trial-5.data
 829-0.txt                   dt.sh        jimmy         Music        snap                    trial-17.data   trial-6.data
 anaconda3                   empty.txt    Jimmy         output.txt  'test.fa?raw=T'          trial-18.data   trial-7.data
 bin                         error.txt    jimy          pg514.txt    trial-10.data           trial-19.data   trial-8.data
```

### Question 6
How can you create in a single command a file containing the contents "Hello, world!" and named universal_greeting.txt?

```bash
echo "hello world"> universal_greetings.txt
```
__output__
```  2014-01-31_JA-america.tsv   829-0.txt     diary.html  '[file]'     home          __MACOSX     pg514.txt   shell-lesson-data.zip
 2014-01_JA.tsv              anaconda3     do           firstdir    jimmy        'man ls'      Pictures    shell-lesson.zip
 2014-02-02_JA-britain.tsv   bin           Documents    for         Jimmy         miniconda3   R           snap
 201403160_01_text.json      date.sh       Downloads    gulliber    jimy          mkdir        seq.txt     universal_greetings.txt
(base) icipe@icipe-HP-Z220-SFF-Workstation:~$ cd universal_greetings.txt
```
### Question 7
What about creating the same file but with filename "universal greeting.txt" (the filename contains a space)?

```bash
echo "hello world"> 'universal greetings'.txt
```
__output__
```  2014-01-31_JA-africa.tsv    33504-0.txt   Desktop      empty.txt   hello-world   jiy          Music       shell-lesson-data          universal_greetings.txt
 2014-01-31_JA-america.tsv   829-0.txt     diary.html  '[file]'     home          __MACOSX     pg514.txt   shell-lesson-data.zip      Videos
 2014-01_JA.tsv              anaconda3     do           firstdir    jimmy        'man ls'      Pictures    shell-lesson.zip
 2014-02-02_JA-britain.tsv   bin           Documents    for         Jimmy         miniconda3   R           snap
 201403160_01_text.json      date.sh       Downloads    gulliber    jimy          mkdir        seq.txt    'universal greetings.txt'
```
### Question 8
How can you use the commandline (on whichever machine you are now, that is connected to the internet) to download directly the 
file you can see on https://github.com/Fnyasimi/my-first-repo/blob/main/directory1/test.fa ? Be careful, you need to get the raw text file itself, 
not the full HTML page presenting it.

```bash
wget https://github.com/Fnyasimi/my-first-repo/blob/main/directory1/test.fa?raw=T
```
__output__
```
--2022-07-26 10:17:32--  https://github.com/Fnyasimi/my-first-repo/blob/main/directory1/test.fa?raw=T
Resolving github.com (github.com)... 140.82.121.4
Connecting to github.com (github.com)|140.82.121.4|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://github.com/Fnyasimi/my-first-repo/raw/main/directory1/test.fa [following]
--2022-07-26 10:17:34--  https://github.com/Fnyasimi/my-first-repo/raw/main/directory1/test.fa
Reusing existing connection to github.com:443.
HTTP request sent, awaiting response... 302 Found
Location: https://raw.githubusercontent.com/Fnyasimi/my-first-repo/main/directory1/test.fa [following]
--2022-07-26 10:17:34--  https://raw.githubusercontent.com/Fnyasimi/my-first-repo/main/directory1/test.fa
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.108.133, 185.199.110.133, 185.199.109.133, ...
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.108.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 831651 (812K) [text/plain]
Saving to: ‘test.fa?raw=T’

test.fa?raw=T                             100%[=====================================================================================>] 812.16K  3.49MB/s    in 0.2s    

2022-07-26 10:17:36 (3.49 MB/s) - ‘test.fa?raw=T’ saved [831651/831651]
```
### Question 9
How can you count the number of lines in this text file (test.fa)? How do you count the number of sequences?

```bash
wc -l test.fa\?raw\=T 
```
__output__

```
10281 test.fa?raw=T
```

### Question 10
Extract only the identifier lines from this file, and write them into a file called "identifiers.txt".

```bash
grep -w ">*" test.fa\?raw\=T identifier.txt
```
__output__
```
test.fa?raw=T:>NM_001361694.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 9, mRNA
test.fa?raw=T:>NM_001361695.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 10, mRNA
test.fa?raw=T:>NM_001164226.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 1, mRNA
test.fa?raw=T:>NM_010938.4 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 6, mRNA
test.fa?raw=T:>AK082580.1 Mus musculus 0 day neonate cerebellum cDNA, RIKEN full-length enriched library, clone:C230066G05 product:nuclear respiratory factor 1, full insert sequence
test.fa?raw=T:>XM_021165121.1 PREDICTED: Mus caroli nuclear respiratory factor 1 (Nrf1), transcript variant X5, mRNA
test.fa?raw=T:>XM_021165122.1 PREDICTED: Mus caroli nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNA
test.fa?raw=T:>AK029034.1 Mus musculus 10 days neonate skin cDNA, RIKEN full-length enriched library, clone:4732483G17 product:nuclear respiratory factor 1, full insert sequence
test.fa?raw=T:>AK014494.1 Mus musculus 14 days embryo liver cDNA, RIKEN full-length enriched library, clone:4432414E03 product:nuclear respiratory factor 1, full insert sequence
test.fa?raw=T:>NM_001361693.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 8, mRNA
test.fa?raw=T:>NM_001361692.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 7, mRNA
test.fa?raw=T:>XM_011241048.1 PREDICTED: Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant X8, mRNA
test.fa?raw=T:>AK031103.1 Mus musculus 13 days embryo forelimb cDNA, RIKEN full-length enriched library, clone:5930405C14 product:nuclear respiratory factor 1, full insert sequence
test.fa?raw=T:>XM_021189475.1 PREDICTED: Mus pahari nuclear respiratory factor 1 (Nrf1), transcript variant X3, mRNA
test.fa?raw=T:>XM_006236198.3 PREDICTED: Rattus norvegicus nuclear respiratory factor 1 (Nrf1), transcript variant X5, mRNA
test.fa?raw=T:>XM_006979405.2 PREDICTED: Peromyscus maniculatus bairdii nuclear respiratory factor 1 (Nrf1), transcript variant X5, mRNA
test.fa?raw=T:>AF098077.1 Mus musculus nuclear respiratory factor-1 (Nrf1) mRNA, complete cds
test.fa?raw=T:>AC161538.7 Mus musculus 6 BAC RP23-1D15 (Roswell Park Cancer Institute (C57BL/6J Female) Mouse BAC Library) complete sequence
test.fa?raw=T:>AC153632.2 Mus musculus 6 BAC RP23-450O1 (Roswell Park Cancer Institute (C57BL/6J Female) Mouse BAC Library) complete sequence
test.fa?raw=T:>XM_017321440.1 PREDICTED: Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant X4, mRNA
test.fa?raw=T:>XM_021189492.1 PREDICTED: Mus pahari nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNA
test.fa?raw=T:>XM_007613569.2 PREDICTED: Cricetulus griseus nuclear respiratory factor 1 (Nrf1), transcript variant X4, mRNA
test.fa?raw=T:>XM_005078088.3 PREDICTED: Mesocricetus auratus nuclear respiratory factor 1 (Nrf1), transcript variant X2, mRNA
test.fa?raw=T:>XM_008762773.2 PREDICTED: Rattus norvegicus nuclear respiratory factor 1 (Nrf1), transcript variant X4, mRNA
test.fa?raw=T:>XM_008846354.2 PREDICTED: Nannospalax galili nuclear respiratory factor 1 (Nrf1), transcript variant X5, mRNA
test.fa?raw=T:>XM_008846355.2 PREDICTED: Nannospalax galili nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNA
test.fa?raw=T:>XM_015998079.1 PREDICTED: Peromyscus maniculatus bairdii nuclear respiratory factor 1 (Nrf1), transcript variant X3, mRNA
test.fa?raw=T:>XM_011241046.2 PREDICTED: Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant X3, mRNA
test.fa?raw=T:>XM_007613561.2 PREDICTED: Cricetulus griseus nuclear respiratory factor 1 (Nrf1), transcript variant X3, mRNA
test.fa?raw=T:>XM_020160204.1 PREDICTED: Castor canadensis nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNA
test.fa?raw=T:>XM_015493834.1 PREDICTED: Marmota marmota marmota nuclear respiratory factor 1 (Nrf1), transcript variant X1, mRNA
test.fa?raw=T:>XM_005365768.2 PREDICTED: Microtus ochrogaster nuclear respiratory factor 1 (Nrf1), transcript variant X4, mRNA
test.fa?raw=T:>XM_021730384.1 PREDICTED: Ictidomys tridecemlineatus nuclear respiratory factor 1 (Nrf1), transcript variant X1, mRNA
test.fa?raw=T:>XM_021237648.1 PREDICTED: Heterocephalus glaber nuclear respiratory factor 1 (Nrf1), transcript variant X3, mRNA
test.fa?raw=T:>XM_021237647.1 PREDICTED: Heterocephalus glaber nuclear respiratory factor 1 (Nrf1), transcript variant X2, mRNA
test.fa?raw=T:>XM_021237646.1 PREDICTED: Heterocephalus glaber nuclear respiratory factor 1 (Nrf1), transcript variant X1, mRNA
test.fa?raw=T:>JN949313.1 Mus musculus targeted non-conditional, lacZ-tagged mutant allele Nrf1:tm1e(KOMP)Wtsi; transgenic
test.fa?raw=T:>JN945378.1 Mus musculus targeted KO-first, conditional ready, lacZ-tagged mutant allele Nrf1:tm1a(KOMP)Wtsi; transgenic
test.fa?raw=T:>XM_021730387.1 PREDICTED: Ictidomys tridecemlineatus nuclear respiratory factor 1 (Nrf1), transcript variant X4, mRNA
test.fa?raw=T:>XM_013503283.1 PREDICTED: Chinchilla lanigera nuclear respiratory factor 1 (Nrf1), transcript variant X9, mRNA
test.fa?raw=T:>XM_013503282.1 PREDICTED: Chinchilla lanigera nuclear respiratory factor 1 (Nrf1), transcript variant X8, mRNA
test.fa?raw=T:>XM_013503281.1 PREDICTED: Chinchilla lanigera nuclear respiratory factor 1 (Nrf1), transcript variant X7, mRNA
test.fa?raw=T:>XM_013503280.1 PREDICTED: Chinchilla lanigera nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNA
test.fa?raw=T:>XM_005402417.2 PREDICTED: Chinchilla lanigera nuclear respiratory factor 1 (Nrf1), transcript variant X4, mRNA
test.fa?raw=T:>XM_014854351.1 PREDICTED: Equus asinus nuclear respiratory factor 1 (NRF1), transcript variant X1, mRNA
test.fa?raw=T:>XM_001502901.6 PREDICTED: Equus caballus nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>XM_008512637.1 PREDICTED: Equus przewalskii nuclear respiratory factor 1 (NRF1), mRNA
test.fa?raw=T:>XM_012789202.2 PREDICTED: Microcebus murinus nuclear respiratory factor 1 (NRF1), transcript variant X7, mRNA
test.fa?raw=T:>XM_008574446.1 PREDICTED: Galeopterus variegatus nuclear respiratory factor 1 (NRF1), mRNA
test.fa?raw=T:>XM_014784894.1 PREDICTED: Ceratotherium simum simum nuclear respiratory factor 1 (LOC101391114), transcript variant X2, mRNA
test.fa?raw=T:>XM_012088037.1 PREDICTED: Cercocebus atys nuclear respiratory factor 1 (NRF1), transcript variant X3, mRNA
test.fa?raw=T:>XM_021730385.1 PREDICTED: Ictidomys tridecemlineatus nuclear respiratory factor 1 (Nrf1), transcript variant X2, mRNA
test.fa?raw=T:>XM_015493835.1 PREDICTED: Marmota marmota marmota nuclear respiratory factor 1 (Nrf1), transcript variant X2, mRNA
test.fa?raw=T:>XM_015448031.1 PREDICTED: Macaca fascicularis nuclear respiratory factor 1 (NRF1), transcript variant X4, mRNA
test.fa?raw=T:>XM_015134910.1 PREDICTED: Macaca mulatta nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>XM_012088036.1 PREDICTED: Cercocebus atys nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>XM_007982896.1 PREDICTED: Chlorocebus sabaeus nuclear respiratory factor 1 (NRF1), transcript variant X7, mRNA
test.fa?raw=T:>XM_007982895.1 PREDICTED: Chlorocebus sabaeus nuclear respiratory factor 1 (NRF1), transcript variant X6, mRNA
test.fa?raw=T:>XM_012088042.1 PREDICTED: Cercocebus atys nuclear respiratory factor 1 (NRF1), transcript variant X7, mRNA
test.fa?raw=T:>XM_012088038.1 PREDICTED: Cercocebus atys nuclear respiratory factor 1 (NRF1), transcript variant X4, mRNA
test.fa?raw=T:>XM_024789577.1 PREDICTED: Macaca nemestrina nuclear respiratory factor 1 (NRF1), transcript variant X11, mRNA
test.fa?raw=T:>XM_021730386.1 PREDICTED: Ictidomys tridecemlineatus nuclear respiratory factor 1 (Nrf1), transcript variant X3, mRNA
test.fa?raw=T:>XM_012088041.1 PREDICTED: Cercocebus atys nuclear respiratory factor 1 (NRF1), transcript variant X6, mRNA
test.fa?raw=T:>XM_012088039.1 PREDICTED: Cercocebus atys nuclear respiratory factor 1 (NRF1), transcript variant X5, mRNA
test.fa?raw=T:>XM_017532570.1 PREDICTED: Cebus capucinus imitator nuclear respiratory factor 1 (NRF1), transcript variant X1, mRNA
test.fa?raw=T:>XM_005550753.2 PREDICTED: Macaca fascicularis nuclear respiratory factor 1 (NRF1), transcript variant X5, mRNA
test.fa?raw=T:>XM_015134909.1 PREDICTED: Macaca mulatta nuclear respiratory factor 1 (NRF1), transcript variant X1, mRNA
test.fa?raw=T:>XM_011723889.1 PREDICTED: Macaca nemestrina nuclear respiratory factor 1 (NRF1), transcript variant X12, mRNA
test.fa?raw=T:>XM_011939585.1 PREDICTED: Colobus angolensis palliatus nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>XM_015134911.1 PREDICTED: Macaca mulatta nuclear respiratory factor 1 (NRF1), transcript variant X3, mRNA
test.fa?raw=T:>XM_011723890.1 PREDICTED: Macaca nemestrina nuclear respiratory factor 1 (NRF1), transcript variant X13, mRNA
test.fa?raw=T:>XM_011995878.1 PREDICTED: Mandrillus leucophaeus nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>XM_015134912.1 PREDICTED: Macaca mulatta nuclear respiratory factor 1 (NRF1), transcript variant X4, mRNA
test.fa?raw=T:>XM_003803318.3 PREDICTED: Otolemur garnettii nuclear respiratory factor 1 (NRF1), mRNA
test.fa?raw=T:>NM_001164227.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 2, mRNA
test.fa?raw=T:>AK037697.1 Mus musculus 16 days neonate thymus cDNA, RIKEN full-length enriched library, clone:A130038J21 product:SIMILAR TO NUCLEAR RESPIRATORY FACTOR 1 homolog [Mus musculus], full insert sequence
test.fa?raw=T:>XM_016958154.2 PREDICTED: Pan troglodytes nuclear respiratory factor 1 (NRF1), transcript variant X7, mRNA
test.fa?raw=T:>XM_021936263.1 PREDICTED: Papio anubis nuclear respiratory factor 1 (NRF1), transcript variant X10, mRNA
test.fa?raw=T:>XM_003813488.3 PREDICTED: Pan paniscus nuclear respiratory factor 1 (NRF1), transcript variant X4, mRNA
test.fa?raw=T:>XM_003896587.4 PREDICTED: Papio anubis nuclear respiratory factor 1 (NRF1), transcript variant X11, mRNA
test.fa?raw=T:>XM_003951129.3 PREDICTED: Pan troglodytes nuclear respiratory factor 1 (NRF1), transcript variant X9, mRNA
test.fa?raw=T:>XM_001155756.5 PREDICTED: Pan troglodytes nuclear respiratory factor 1 (NRF1), transcript variant X8, mRNA
test.fa?raw=T:>XM_017957164.2 PREDICTED: Papio anubis nuclear respiratory factor 1 (NRF1), transcript variant X12, mRNA
test.fa?raw=T:>XM_021673680.1 PREDICTED: Aotus nancymaae nuclear respiratory factor 1 (NRF1), transcript variant X1, mRNA
test.fa?raw=T:>XM_010378768.1 PREDICTED: Rhinopithecus roxellana nuclear respiratory factor 1 (NRF1), transcript variant X1, mRNA
test.fa?raw=T:>XM_010378771.1 PREDICTED: Rhinopithecus roxellana nuclear respiratory factor 1 (NRF1), transcript variant X4, mRNA
test.fa?raw=T:>XM_017321441.1 PREDICTED: Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNA
test.fa?raw=T:>XM_021673683.1 PREDICTED: Aotus nancymaae nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>XM_010378770.1 PREDICTED: Rhinopithecus roxellana nuclear respiratory factor 1 (NRF1), transcript variant X3, mRNA
test.fa?raw=T:>XM_010378769.1 PREDICTED: Rhinopithecus roxellana nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>NM_001164230.1 Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant 5, mRNA
test.fa?raw=T:>XM_024250195.1 PREDICTED: Pongo abelii nuclear respiratory factor 1 (NRF1), transcript variant X1, mRNA
test.fa?raw=T:>XM_006505006.3 PREDICTED: Mus musculus nuclear respiratory factor 1 (Nrf1), transcript variant X5, mRNA
test.fa?raw=T:>XM_010378772.1 PREDICTED: Rhinopithecus roxellana nuclear respiratory factor 1 (NRF1), transcript variant X5, mRNA
test.fa?raw=T:>XM_024250197.1 PREDICTED: Pongo abelii nuclear respiratory factor 1 (NRF1), transcript variant X3, mRNA
test.fa?raw=T:>XM_024250196.1 PREDICTED: Pongo abelii nuclear respiratory factor 1 (NRF1), transcript variant X2, mRNA
test.fa?raw=T:>L22454.1 Homo sapiens nuclear respiratory factor-1 (NRF-1) mRNA, complete cds
test.fa?raw=T:>AK134483.1 Mus musculus 11 days embryo head cDNA, RIKEN full-length enriched library, clone:6230412K09 product:nuclear respiratory factor 1, full insert sequence
test.fa?raw=T:>U02683.1 Homo sapiens alpha palindromic binding protein mRNA, complete cds
test.fa?raw=T:>NM_001040110.1 Homo sapiens nuclear respiratory factor 1 (NRF1), transcript variant 2, mRNA
``

### Question 11
How can you process the file you got from question 8 to replace all its uppercase "A" letters into lowercase "a" letters, leaving the rest untouched?

```bash
grep "A" test.fa\?raw\=T | tr [A] [a]
```
__output__
```
>XM_021165122.1 PREDICTED: Mus caroli nuclear respiratory factor 1 (Nrf1), transcript variant X6, mRNa
CTCGGCGGCGGCGGCGGCGGCaGaGGCGGCaGCGCTCGCCaTTGCCGCTGGTGGCaGGaGGCTGCGaGGaGCCGGCGCGG
TCGCaGTCTCCaCGGCGCaGGCCCaCGGTaGCGCaGCCGCTCTGaGGTCGaaTGaTaTGTGGTTCaTGTaGaCCaCaTTT
TGTTTCCCaCTCaCCCaTTGaTGGaCaCTTGGGTaGCTTCCaTCTTTTGGCTGTTGTGaaTaaTGCTGCTaTGaaCaTGG
GTGTGCaCaTaGCTCTCTGaGaCGCTGCTTTCaGTCCTTCTGGTaGaTCTTCaTGGaGGaGCaCGGaGTGaCCCaaaCTG
```
### Question 12
In one command, ask for the display of all identifier lines from the same file test.fa without wrapping the lines, i.e. by having all lines displayed 
on your screen effectively start with the character '>'.

```bash
less -S identifiers.txt
```

### Question 13
Can you write a very short script (possibly one single commandline) to extract from the same file the species names?

```bash
cut -d ' ' -f2-4 identifiers.txt |cut -d : -f 2 | sed 's/^ *//g' | cut -d ' ' -f 1,2
```

### Question 14
Once this is done, how do you count the species names with their order of multiplicity 
(i.e. how many sequences belong to Mus musculus, how many to Homo sapiens, etc)?

```bash
 cut -d ' ' -f2-4 identifiers.txt |cut -d : -f 2 | sed 's/^ *//g' | cut -d ' ' -f 1,2 | uniq -c |sort -n
```

### Question 15
Write a loop in Bash producing all the integers from 1 to 30, one per line?

```bash
$ for numbers in 1 30 ; 
> do
seq $numbers ; 
> done
```

### Question 16
Create at once 20 files called "trial1" to "trial20" and *then* rename them all by appending the suffix ".data". 
Of course, don't issue 20 commands, but just one.

```bash
touch trial-{1..20}.data
```
__output__
```
 2014-01-31_JA-africa.tsv    829-0.txt    do          for           jimy         mkdir       shell-lesson-data       trial-11.data   trial-17.data   trial-3.data   trial-9.data
 2014-01-31_JA-america.tsv   anaconda3    Documents   gulliber      jiy          Music       shell-lesson-data.zip   trial-12.data   trial-18.data   trial-4.data  'universal greetings.txt'
 2014-01_JA.tsv              bin          Downloads   hello-world   less         pg514.txt   shell-lesson.zip        trial-13.data   trial-19.data   trial-5.data   universal_greetings.txt
 2014-02-02_JA-britain.tsv   date.sh      empty.txt   home          __MACOSX     Pictures    snap                    trial-14.data   trial-1.data    trial-6.data   Videos
 201403160_01_text.json      Desktop     '[file]'     jimmy        'man ls'      R          'test.fa?raw=T'          trial-15.data   trial-20.data   trial-7.data
 33504-0.txt                 diary.html   firstdir    Jimmy         miniconda3   seq.txt     trial-10.data           trial-16.data   trial-2.data    trial-8.data
```

### Question 17
Try this with the command "expr 1 / 0", whose purpose is to calculate the integer result of 1 divided by 0. What happens? Why?
```output
expr: division by zero
```
### Question 18
How can you separately redirect the standard output and the standard error streams into two separate files?

```bash
command 2> error.txt 1> output.txt
```

### Question 19
Write a Bash script asking "What's your name?", then waiting for you (the user) to enter you name and press Enter, 
following what the program displays some text according to the following pattern:
"Good morning/day/evening, your_name!
It's now current_time on this lovely day of current_day." and it exits.

For instance, the message written by your program would be:
```
Good day Emmanuel! It's not 12:57EAT on this lovely day of July 20. 1:00
or 'Good morning" in the morning hours, or "Good evening" in the evening hours, depending on the current time.
Of course there will be at least an if or a case construct in your script.
```

### Question 20
Suppose your current working directory is /home/icipe/Linux/Exercises/. What is the command that will enable to move to /home/icipe/Fun_stuff/?

```bash
cd ../../Fun_stuff/
```
