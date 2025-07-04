# Examples

This section provides example runs for each type of reaction in the Gibson Assembly Assistant.

## Plasmid Linearization / Insert Preparation

### Input:

- What type of PCR reaction are you planning? → **Plasmid linearization / Insert preparation**
- Do you know the melting temperatures (Tm) of your primers? → **Yes**
- Enter the Tm of your forward primer (in °C) → **60.1**
- Enter the Tm of your reverse primer (in °C) → **57.8**
- Do you know the size of your DNA sequence? → **Yes**
- Enter the DNA size (in bp) → **10857**
- Enter the number of samples → **1**
- Are you linearizing a plasmid or preparing an insert with overhangs? → **Linearizing a plasmid**

### Output:

<pre>Annealing temperature               53.95 °C
Elongation time                     1:49 min
Phanta master mix                   25 µL
ddH₂O                               25 µL
Forward primer (undiluted)          1 µL
Reverse primer (undiluted)          1 µL
DNA amount                          2 µL</pre>

## Ligation

### Input:

- What type of PCR reaction are you planning? → **Ligation**
- Do you know the size of your linearized vector? → **Yes**
- Enter the linearized vector size (in bp) → **10857**
- Enter the concentration of the linearized vector (in ng/µL) → **70**
- Do you know the size of your insert (with overhangs)? → **No**
- Enter the path or filename of the text file containing the insert sequence (including overhangs) → **dna_seq_example.txt**
- Enter the concentration of the insert (in ng/µL) → **140**

### Output:

<pre>Enzyme mix                          7.5 µL
Vector dilution                     1:2
Insert dilution                     1:8
Vector                              1.86 µL
Insert                              1.12 µL
Attention                           None</pre>

* An Attention note will appear when the volume of either the vector or the insert needs to be reduced to keep the total reaction volume within the 3 µL limit.


## Colony PCR

### Input:

- What type of PCR reaction are you planning? → **Colony PCR**
- Do you know the melting temperatures (Tm) of your primers? → **No**
- Enter the sequence of your forward primer → **gttagagggagctctgatcactgagGGAGATGCAGTGAGTGGGTGAACGG**
- Enter the sequence of your reverse primer → **CAATTCCTTGTCTTCTCTGATACAGtttaagagacgcaaccacaacgctc**
- Do you know the size of your DNA sequence? → **No**
- Enter the path or filename of your DNA sequence text file (including primers) → **dna_seq_example.txt**
- Enter the number of samples → **3**

### Output:

<pre>Annealing temperature               65.35 °C
Elongation time                     16.34 sec
Phanta master mix                   21 µL
ddH₂O                               21 µL
Forward primer (1:10 dilution)      3 µL
Reverse primer (1:10 dilution)      3 µL
Colony                              Add manually</pre>

---

* For each experiment, you will also be asked to enter an experiment name, and you can choose to generate a '.docx' file of the protocol. This file will be saved in the same folder as the script.
* You can test these examples using the provided **dna_seq_example.txt** file.
