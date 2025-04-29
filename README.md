# A Fungus Among Us: Retrospective Fungi in Maryland's Computational Survey of Chtrid 

## Jackson McClean


## Abstract 

For my SMP, I did an analysis of whether previous and current amphibians across Southern Maryland were/are exposed to chytrid fungi. For this project, I focused on my data where I swabbed 83 preserved amphibians in the museum collection. Using previous lessons in this course, I made a dictionary listing all the amphibian species I sampled and how many of them were in the museum. I also added how many total swabs I took from each species and the total percentage they make up my dataset. Northern Green Frogs (Rana clamitans melanota) were the most sampled species, with 20 individuals, 60 swabs, and making up nearly a quarter of my data. In future studies, I would like to add a loop to determine the number of times each amphibian appeared to reduce the length of my sequence data. I would also like to calculate standard deviation and error for my species if I were to vary the number of swabs I took for each individual.


## Introduction

For my SMP, I wanted to study a group of animals I was unfamiliar with. This led me to decide if I wanted to study amphibians or reptiles. I was undecided until I took a conservation biology class last summer. I had a class where I was learning about the different conservation methods from species across the globe, and one of the videos was based in Panama.

In this video, Panama's national frog, the Panaminian Golden Frog (Atelopus zeteki) was suffering from rapid population decline dating back to the 1980s (Nature on PBS 2024). Some of the recent deceased frogs the researchers found were covered in a white fuzz and were gaunt or deathly underweight (Nature on PBS 2024). The researchers determined based on the symptoms of the deceased frogs that they were sick with a fungal disease, specifically chytrid. 

Chytrid is becoming more prevalent in amphibians (Amphibia Web 2009). The main reason is the global increase in temperatures and rainfall, which both promote increased fungal growth (Sun et al. 2020). When mature, these fungi release spores into water, typically where amphibians lay their eggs so they don't dry out (Salice et al. 2011). Once bound to an amphibian, the chytrid spores "eat" at proteins responsible for providing structure in amphibian skin (Kilpatrick et al. 2010). This structure is critical as amphibians rely on their skin for breathing and allowing water to travel across their bodies (Kilpatrick et al. 2010). If these proteins are destroyed, then the skin layers collapse, which makes breathing difficult and blocks water transport to organs, dehydrating amphibians (Fischer and Garner 2020). For animals that rely on their skin for breathing, this is a serious problem.

During my SMP, I sampled water from 5 state parks across Southern Maryland to determine if chytrid is present in the area. However, I did not finish these results due to time constraints. The other part of my project was swabbing preserved amphibians. I kept a Google Sheet of all the amphibians I sampled, recording their date of preservation and what species they were. For this project in particular, I wanted to make a dictionary of all my amphibian species to save for convience. I also wanted to make a table with each species, what dictionary letter they are, and how many of that species were swabbed. Lastly, I wanted to make a table that has the toal number of swabs per species and the percentage they make up in total. 


## Methods/Results

> Part 1: Making the Dictionary

For this part of my project, I made a dictionary for all the amphibians I swabbed in the POB Museum. There were 83 samples, but I couldn't ID two (one was too small, and the other was just muscle and bone). I made a program called `SMPdictionary.py`, with code that is similar to the amino acid dictionary program (`proteincalc.py`):

```
#!/usr/bin/python3

AmphibSeq = "AAAGGGBBTPPIIPIIPIIIIOFOBGRSCCCGGCCWTTTTOGCDHFDPPPPPIAIIBGGBGGGGGBGGGBBBYGGGBBYYG"
for Amphibian in AmphibSeq:
        print(Amphibian)
AmphibSeq
```

I used `touch` to make the program and `nano` to edit it. I also used `chmod +x` to make the program executable. The single letters are abbreviations for each of my sampled species (which are as follows):

A - Axolotl

G - Northern Green Frog

B - Bullfrog

T - American Toad

P - Pickerel Frog

I - Northern Leopard Frog (I for *Lithobates pipiens*)

O - Southern Leopard Frog (O for *Lithobates sphenocephalus*)

F - Fowler's Toad

R - Red-backed Salamander

S - Spotted Salamander

C - Northern Cricket Frog

W - Woodhouse Toad

D - Northern Dusky Salamander

H - American Green Tree Frog (H is for Hylidae, which contains tree frogs)

Y - Wood Frog (Y is a letter in its scientific name, *Lithobates sylvaticus*)

This is a ton of samples, so making a table would make this easier on the eyes :)

### HTML Dictionary

To make the dictionary into a nice table, I converted my dictionary into HTML code. Here's the HTML editor I used (shoutout to Dr. Salerno for providing the website!): [HTML Online Editor](https://www.w3schools.com/html/html_editor.asp). For the table code, I looked back and copied the source code from http://practicalcomputing.org/aminoacid.html (I did this by opening the HTML site, right-clicking the page, and then clicking "View Page Source").

Here's the table edited to include my SMP data. All species are put in alphabetical order based on their scientific names.

<div>
<!DOCTYPE html>
<html><head><title>AMPHIBIAN SAMPLING</title></head>
<body>
<font face="Helvetica,Arial">
<table rules=all cellpadding=4>
<tr><td>Common Name</td><td> Scientific Name</td><td> Dictionary Letter</td><td> Number of Samples</td></tr>
<tr><td>Northern Cricket Frog</td><td><i>Acris crepitans<i></td><td>C</td><td>7</td></tr>
<tr><td>Spotted Salamander</td><td><i>Ambystoma maculatum<i></td><td>S</td><td>1</td></tr>
<tr><td>Axolotl</td><td><i>Ambystoma mexicanum<i></td><td>A</td><td>4</td></tr>
<tr><td>American Toad</td><td><i>Anaxyrus americanus<i></td><td>T</td><td>5</td></tr>
<tr><td>Fowler's Toad</td><td><i>Anaxyrus fowleri<i></td><td>F</td><td>2</td></tr>
<tr><td>Woodhouse Toad</td><td><i>Anaxyrus woodhousii<i></td><td>W</td><td>1</td></tr>
<tr><td>Northern Dusky Salamander</td><td><i>Desmognathus fuscus<i></td><td>D</td><td>2</td></tr>
<tr><td>American Green Tree Frog</td><td><i>Hyla cinerea<i></td><td>H</td><td>1</td></tr>
<tr><td>American Bullfrog</td><td><i>Lithobates catesbeianus<i></td><td>B</td><td>11</td></tr>
<tr><td>Pickerel Frog</td><td><i>Lithobates palustris<i></td><td>P</td><td>9</td></tr>
<tr><td>Northern Leopard Frog</td><td><i>Lithobates pipiens<i></td><td>I</td><td>11</td></tr>
<tr><td>Southern Leopard Frog</td><td><i>Lithobates sphenocephalus<i></td><td>O</td><td>3</td></tr>
<tr><td>Wood Frog</td><td><i>Lithobates sylvaticus<i></td><td>Y</td><td>3</td></tr>
<tr><td>Red-Backed Salamander</td><td><i>Plethodon cinereus<i></td><td>R</td><td>1</td></tr>
<tr><td>Northern Green Frog</td><td><i>Rana clamitans melanota<i></td><td>G</td><td>20</td></tr>

</table>
</font>
</body>
</html>

</div>

### Converting the Table to Python3 Format

Now, I want to make the table above into a python3-friendly dictionary. To do so, I copied my source code that I used to make my table and put it into a text editor (Sublime Text). Here's what the source code looks like:

```
<tr><td>Common Name</td><td><i>Scientific Name<i></td><td> Dictionary Letter</td><td> Number of Samples</td></tr>
<tr><td>Northern Cricket Frog</td><td><i>Acris crepitans<i></td><td>C</td><td>7</td></tr>
<tr><td>Spotted Salamander</td><td><i>Ambystoma maculatum<i></td><td>S</td><td>1</td></tr>
<tr><td>Axolotl</td><td><i>Ambystoma mexicanum<i></td><td>A</td><td>4</td></tr>
<tr><td>American Toad</td><td><i>Anaxyrus americanus<i></td><td>T</td><td>5</td></tr>
<tr><td>Fowler's Toad</td><td><i>Anaxyrus fowleri<i></td><td>F</td><td>2</td></tr>
<tr><td>Woodhouse Toad</td><td><i>Anaxyrus woodhousii<i></td><td>W</td><td>1</td></tr>
<tr><td>Northern Dusky Salamander</td><td><i>Desmognathus fuscus<i></td><td>D</td><td>2</td></tr>
<tr><td>American Green Tree Frog</td><td><i>Hyla cinerea<i></td><td>H</td><td>1</td></tr>
<tr><td>American Bullfrog</td><td><i>Lithobates catesbeianus<i></td><td>B</td><td>11</td></tr>
<tr><td>Pickerel Frog</td><td><i>Lithobates palustris<i></td><td>P</td><td>9</td></tr>
<tr><td>Northern Leopard Frog</td><td><i>Lithobates pipiens<i></td><td>I</td><td>11</td></tr>
<tr><td>Southern Leopard Frog</td><td><i>Lithobates sphenocephalus<i></td><td>H</td><td>3</td></tr>
<tr><td>Wood Frog</td><td><i>Lithobates sylvaticus<i></td><td>Y</td><td>3</td></tr>
<tr><td>Red-Backed Salamander</td><td><i>Plethodon cinereus<i></td><td>R</td><td>1</td></tr>
<tr><td>Northern Green Frog</td><td><i>Rana clamitans melanota<i></td><td>G</td><td>20</td></tr>
```

I want to format my code to have the dictionary letter and the number of samples I had. This is the format I'm looking for:

```
'A':4,
```

In this example, 'A' is for Axolotl, and I sampled 4 of them. To accomplish this, I used the find and replace text editing! Here is my find and replace code:

```
Find:.+(.)</td><td>([\w\.]+).+
Replace:'\1':\2,
```

**Find:** `.+(.)` captures the whole line of code, which I don't want. `</td><td>` highlights the `<tr><td>Common Name</td><td><i>` in each line (which I want to delete). `([\w\.]+)` captures the scientific name, dictionary letter, and number of samples for each species (great since `\w\` searches for both the dictionary letters and sample numbers!) Ending the line with `.+` matches the `</td></tr>` at the end of each sample line.

Replace: `'\1'` will place the dictionary letter of each sample into single quotation marks. `:\2,` will print the number of samples after a colon (`:`) and before a comma (`,`).

Here's my new dictionary:

```
<tr><td>Common Name</td><td><i>Scientific Name<i></td><td> Dictionary Letter</td><td> Number of Samples</td></tr>
'C':7,
'S':1,
'A':4,
'T':5,
'F':2,
'W':1,
'D':2,
'H':1,
'B':11,
'P':9,
'I':11,
'H':3,
'Y':3,
'R':1,
'G':20,
```

I'm almost there! I went back to Sublime Text and made some more changes. First, I deleted the first line (no find and replace needed) and typed `AmphibDict={`. I placed the closing curly bracket under the 'G' line. Here's what the completed dictionary looks like now:

```
AmphibDict={
'C':7,
'S':1,
'A':4,
'T':5,
'F':2,
'W':1,
'D':2,
'H':1,
'B':11,
'P':9,
'I':11,
'H':3,
'Y':3,
'R':1,
'G':20,
}
```

### Running `SMPdictionary.py` with `AmphibDict`

I went back to SMPdictionary.py and added my AmphibDict to the program before AmphibSeq appeared. Here's what the program looks like:

```
#!/usr/bin/python3

AmphibDict={
'C':7,
'S':1,
'A':4,
'T':5,
'F':2,
'W':1,
'D':2,
'H':1,
'B':11,
'P':9,
'I':11,
'H':3,
'Y':3,
'R':1,
'G':20,
}

AmphibSeq = "AAAGGGBBTPPIIPIIPIIIIOFOBGRSCCCGGCCWTTTTOGCDHFDPPPPPIAIIBGGBGGGGGBGGGBBBYGGGBBYYG"
for Amphibian in AmphibSeq:
        print(Amphibian, AmphibDict[Amphibian])
```

And here's the output:

```
./SMPdictionary.py
A 4
A 4
A 4
G 20
G 20
G 20
B 11
B 11
T 5
P 9
P 9
I 11
I 11
P 9
I 11
I 11
P 9
I 11
I 11
I 11
I 11
O 3
F 2
O 3
B 11
G 20
R 1
S 1
C 7
C 7
C 7
G 20
G 20
C 7
C 7
W 1
T 5
T 5
T 5
T 5
O 3
G 20
C 7
D 2
H 1
F 2
D 2
P 9
P 9
P 9
P 9
P 9
I 11
A 4
I 11
I 11
B 11
G 20
G 20
B 11
G 20
G 20
G 20
G 20
G 20
B 11
G 20
G 20
G 20
B 11
B 11
B 11
Y 3
G 20
G 20
G 20
B 11
B 11
Y 3
Y 3
G 20
```

This is a very long list, but the number of individuals sampled from each species appears.
---
> Part 2: Descriptive Stats

For the second part of my final project, I want to look at the mean number of swabs (+/- SE) for each species I sampled. For all 83 samples (81 identified species with 2 unidentified), I took 3 swabs per sample.

### Making the .csv file

To run this part in Python3, I made a .csv file formatted as shown in this tutorial: [Programming with Python: Analyzing Patient Data](https://swcarpentry.github.io/python-novice-inflammation/02-numpy.html). My `.csv` contains all the swab numbers (3); nothing more. I put a 0 in for the 2 unidentified species as I did not include them in my dictionary. The file is named `Swabbing.csv` (original, I know), and I moved it from my downloads to my `computing-SP25-course-content` folder so my terminal can find it.

### Importing Numpy

In my terminal, I typed python3 to go into Python. I then typed `import numpy`, well, import numpy (a program that can run number-heavy processes like calculating means, standard deviation (SD), standard error (SE), etc.).

### Reading `Swabbing.csv`

I typed the following to read my `.csv` file to find the number of swabs per individual:

```
numpy.loadtxt(fname='Swabbing.csv', delimiter=',') # Loads Swabbing.csv and separates each row by commas
array([3., 3., 3., 3., 3., 3., 3., 0., 3., 3., 3., 3., 3., 3., 3., 3., 3.,
       3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3.,
       3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3.,
       3., 3., 0., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3.,
       3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3., 3.])
data = numpy.loadtxt(fname='Swabbing.csv', delimiter=',') # Renames my file ad data
print(data) # Prints the Swabbing Data
[3. 3. 3. 3. 3. 3. 3. 0. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3.
 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3.
 3. 3. 3. 3. 3. 0. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3.
 3. 3. 3. 3. 3. 3. 3. 3. 3. 3. 3.]
```

### Calculating Mean, SD, and SE for the Whole Dataset

I calculated the mean, SD, and SE from my whole dictionary. I used this website to calculate SE: [How to Calculate the Standard Error of the Mean in Python.](https://www.statology.org/standard-error-of-mean-python/)

```
print(numpy.mean(data)) # Prints the mean of the whole dataset
2.927710843373494
stdval = numpy.std(data) # Defines the SD of the whole dataset
print(stdval) # Prints the SD of the whole dataset
0.46004537571172976
SE = stdval/numpy.sqrt(numpy.size(data)) # Defines SE
stdval/numpy.sqrt(numpy.size(data)) # Calculates the SE of the whole dataset
0.05049654022667708
```

### Calculating the Total Number of Samples from Each Species

I was going to calculate the mean, SD, and SE for each species, but I realized that all of my samples had 3 swabs taken from (the zeroes are the species that couldn't be identified). I calculated the mean for each species and took the total number of swabs instead.

Here's an example of what I described initially:

```
A = numpy.array([3,3,3,3]) # A is for Axolotl, and there were 4 of them
print(numpy.mean(A))
3.0
stdval = numpy.std(A)
print(stdval)
0.0 
SE = stdval/numpy.sqrt(numpy.size(A))
print(SE)
0.0
```

As seen above, all the swab values are 3, which means there is no standard deviation and, ultimately no standard error. The mean I can still use, however:

```
Total = sum(A) # Adds all the array values together
print(Total)
12 # 12 total swabs were taken from 4 Axolotls
```

I calculated the mean and total number of swabs for all species, which is shown below and in a table for convenience. I calculated the % of total sample size by taking the number of individuals sampled and divided that number by 83.

```
C = numpy.array([3,3,3,3,3,3,3])
print(numpy.mean(C))
3.0
Total = sum(C)
print(Total)
21

S = numpy.array([3])
print(numpy.mean(S))
3.0
Total = sum(S)
print(Total)
3


Axolotls are shown earlier :)

T = numpy.array([3,3,3,3,3])
print(numpy.mean(T))
3.0
Total = sum(T)
print(Total)
15

F = numpy.array([3,3])
print(numpy.mean(F))
3.0
Total = sum(F)
print(Total)
6

W = numpy.array([3])
print(numpy.mean(W))
3.0
Total = sum(W)
print(Total)
3

D = numpy.array([3,3])
print(numpy.mean(D))
3.0
Total = sum(D)
print(Total)
6

H = numpy.array([3])
print(numpy.mean(H))
3.0
Total = sum(H)
print(Total)
3

B = numpy.array([3,3,3,3,3,3,3,3,3,3,3])
print(numpy.mean(B))
3.0
Total = sum(B)
print(Total)
33

P = numpy.array([3,3,3,3,3,3,3,3,3])
print(numpy.mean(P))
3.0
Total = sum(P)
print(Total)
27


I = numpy.array([3,3,3,3,3,3,3,3,3,3,3])
print(numpy.mean(I))
3.0
Total = sum(I)
print(Total)
33

H = numpy.array([3,3,3])
print(numpy.mean(H))
3.0
Total = sum(H)
print(Total)
9

Y = numpy.array([3,3,3])
print(numpy.mean(Y))
3.0
Total = sum(Y)
print(Total)
9

R = numpy.array([3])
print(numpy.mean(Y))
3.0
Total = sum(R)
print(Total)
3

G = numpy.array([3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3,3])
print(numpy.mean(G))
3.0
Total = sum(G)
print(Total)
60
```

| Common Name | Scientific Name | Dictionary Letter | Total # of Samples | % of total sample size (n = 83, before x 100) |
| --- | --- | --- | --- | --- |
| Northern Cricket Frog | *Acris crepitans* | C   | 21  | 0.08433734939759036 |
| Spotted Salamander | *Ambystoma maculatum* | S   | 3   | 0.012048192771084338 |
| Axolotl | *Ambystoma mexicanum* | A   | 12  | 0.04819277108433735 |
| American Toad | *Anaxyrus americanus* | T   | 15  | 0.060240963855421686 |
| Fowler's Toad | *Anaxyrus fowleri* | F   | 6   | 0.024096385542168676 |

| Common Name | Scientific Name | Dictionary Letter | Total # of Samples | % of total sample size (n = 83, before x 100) |
| --- | --- | --- | --- | --- |
| Woodhouse Toad | *Anaxyrus woodhousii* | W   | 3   | 0.012048192771084338 |
| Northern Dusky Salamander | *Desmognathus fuscus* | D   | 6   | 0.024096385542168676 |
| American Green Tree Frog | *Hyla cinera* | H   | 3   | 0.012048192771084338 |
| American Bullfrog | *Lithobates catesbeianus* | B   | 33  | 0.13253012048192772 |
| Pickerel Frog | *Lithobates palustris* | P   | 27  | 0.10843373493975904 |

| Common Name | Scientific Name | Dictionary Letter | Total # of Samples | % of total sample size (n = 83, before x 100) |
| --- | --- | --- | --- | --- |
| Northern Leopard Frog | *Lithobates pipiens* | I   | 33  | 0.13253012048192772 |
| Southern Leopard Frog | *Lithobates sphenocephalus* | O   | 9   | 0.03614457831325301 |
| Wood Frog | *Lithobates sylvaticus* | Y   | 9   | 0.03614457831325301 |
| Red-Backed Salamander | *Plethodon cinereus* | R   | 3   | 0.012048192771084338 |
| Northern Green Frog | *Rana clamitans melanota* | G   | 60  | 0.24096385542168675 |

## Discussion/Conclusions

As shown above, I was able to make my dictionary, table of each species and the number of times that they appeared, and the percentages they made up in my study. As shown in part 2, of my methods, Northern Green Frogs made up most of my data, appearing 20 times, taking 60 swabs, and comprising almost a quarter of my total samples. 

One of the shortcomings I had in this project came in part 2 of my methods. I initally wanted to calculate the standard deviation and standard error from the number of swabs from each individual. However, I found that I took 3 swabs for every individual (including the 2 frogs that I couldn't identify). I got a value of zero for both standard deviation and error. This is due to all the 3's in my dataset, where there isn't any deviation. I would like to run this project again with different numbers of swabs per species to see if there was any variation in swabbing. 

Another important note about this project was that it took many months to learn the programming. Prior to this year, I never coded in the Terminal and had minimal experience in Python3. For the dictionary specifically, I based my data in part 1 from an example with amino acids (Haddock and Dunn 2011). It's also important to have the most recent updates for Python3 as some packages such as numpy may not be available in older Python versions (Haddock and Dunn 2011). 

If I could learn something new to improve the project, I would want to learn arrays more. In part 2, I was unable to make arrays for species that appeared at different points in my dictionary. For example, the Axolotl appeared in my first 3 entries and then appeared again at entry 54. When I tried to splice my array into [1:4, 53:54], I was recieving error messages. I would like to do this to define the swab entries for each dictionary letter to make calculating the mean easier (as in less code to type). 

## Acknowledgements

I would like to thank Dr. Patricia Salerno for teaching me this semester about all the different coding techniques in Python, Terminal, and GitHub. I would also like to thank my computing class for helping me troubleshoot errors with my code and different ways to solve problems. Lastly, I would like to thank Dr. Abby Beatty for her guidance during my SMP and letting me use my data for this computing project.  

## References cited  

Amphibia Web. 2009. Chytrid swabbing protocol. Website https://amphibiaweb.org [Accessed 23 February 2025].

Fischer, M. C. and T. W. J. Garner. 2020. Chytrid fungi and global amphibian declines. Nature Reviews Microbiology 18: 332-343.

Haddock, S. H. D. and C. W. Dunn. Chapter 7: Components of Programming. *In* S. H. D. Haddock and C. W. Dunn [eds.], Practical Computing for Biologists. Sinauer Associates, Inc. X Publishers, Sunderland, Massachusetts, U.S.A.

Kilpatrick, A. M., C. J. Briggs, and P. Daszak. 2010. The ecology and impact of chytridiomycosis: an emerging disease of amphibians. Trends in Ecology and Evolution 25: 109-118.

Nature on PBS. 2024. Frogs are going extinct - here's how we can save them | WILD HOPE. YouTube. Website https://www.youtube.com/watch?v=WXK6fTluM48 [accessed 28 Apr 2025].

Salice, C. J., C. L. Rowe, J. H. K. Pechmann, and W. A. Hopkins. 2011. Multiple stressors and complex life cycles: insights from a population-level assessment of breeding site contamination and terrestrial habitat loss in an amphibian. Environmental Toxiology and Chemistry 30: 2874-2882. 

Sun, S., M. J. Hoy, and J. Heitman. 2020. Fungal Pathogens. Current Biology 30: 1163-1169. 
