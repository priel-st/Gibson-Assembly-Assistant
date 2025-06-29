# Gibson Assembly Assistant

## Introduction

Gibson Assembly is a widely used molecular cloning method that enables the joining of multiple DNA fragments in a single, isothermal reaction. It has become an essential tool in synthetic biology and genetic engineering due to its efficiency and flexibility.  
Molecular cloning involves assembling recombinant DNA molecules and introducing them into host organisms (typically laboratory strains of *Escherichia coli*) for replication and propagation.

A typical Gibson Assembly workflow involves several steps:
- Linearizing the desired vector and adding overhangs to the insert using PCR.  
- Running the DNA on a gel and purifying the fragments.  
- Ligating the vector and insert in a Gibson reaction.  
- Transforming the construct into *E. coli* and plating the cells.  
- Performing colony PCR to identify positive colonies.  
- Growing starters and purifying the resulting plasmid, which can then be used as-is or be further modified.  

A core technique in this workflow is the **Polymerase Chain Reaction (PCR)**, which allows amplifying DNA sequences. The PCR process consists of repeating temperature cycles, made up of three main steps:

1. **Denaturation**  
   The double-stranded DNA is heated (typically to ~95°C) to separate it into two single strands.

2. **Annealing**  
   The temperature is lowered to allow primers (short DNA sequences complementary to the target region) to bind (anneal) to the single-stranded template DNA.

3. **Elongation**  
   The temperature is raised to the optimal level for DNA polymerase (usually Taq), which extends the primers by synthesizing new DNA strands complementary to the templates.

These steps are repeated for 20–40 cycles, leading to exponential amplification of the target DNA sequence.

## What Does This Project Do?

This project is a virtual assistant for planning Gibson Assembly experiments. In a typical Gibson Assembly workflow, several PCR-based steps are required:

- Plasmid linearization and preparation of DNA inserts with overhangs.
- Ligation of the plasmid and inserts.
- Colony PCR to identify positive colonies.  

Each of these steps requires specific reaction components and calculations - including annealing temperatures, elongation times, and reagent volumes based on DNA concentrations.
This tool automates the process, helping users quickly and accurately calculate the necessary parameters for each PCR step involved in Gibson Assembly. The goal is to reduce setup time, minimize errors, and provide a consistent planning workflow for molecular biology experiments.

## User Input

The tool interacts with the user via the command line and collects information required to plan different PCR-based steps involved in Gibson Assembly. The user is prompted to provide details such as:

- The **type of reaction** (e.g., plasmid linearization, insert amplification, colony PCR).  
- **Primer sequences** or their **melting temperatures (Tm)**. 
- The **DNA sequence** (via a .txt file) or the **length (in base pairs)** of the template.  
- The **number of samples or reactions** to prepare.  
- Any additional relevant parameters depending on the selected reaction type.  

## Output

The tool provides the user with:

- A **command-line summary** displaying all calculated parameters, including reagent volumes, annealing temperatures, and elongation times, for quick reference.  
- A **.docx file** that serves as a complete PCR protocol, including all relevant inputs and calculated values.

## Technical Information and Installation

This project is written in **Python 3.8+**.

### Installation

1. Clone this repository:
<pre>git clone https://github.com/priel-st/Gibson-Assembly-Assistant.git
cd Gibson-Assembly-Assistant</pre>

2. Install required libraries:
<pre>pip install -r requirements.txt</pre>

### Running the Tool

Use the following command in the terminal:
<pre>python gibson_assembly_assistant.py</pre>

---

This project was created as part of the [Python programming course](https://github.com/Code-Maven/wis-python-course-2025-03) at the [Weizmann Institute of Science](https://www.weizmann.ac.il/pages/).  
