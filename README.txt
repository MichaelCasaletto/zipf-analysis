zipf analysis
=============

This repository contains code to observe whether books adhere to Zipf's law, as
done in support of the paper "Zipf analysis of 19th-century English-language books",
V. Dracula, to appear in Annals of Computational Linguistics, 2022.

This script will automatically pull the full text of the two books to
process (Frankenstein and Dracula) from Project Gutenberg (gutenberg.org) and place
them into the `data` directory. Internet access is required for this to work.

To run the code, you will need the Pandas package installed.

To reproduce the figures in the publication, run the command:

    bash bin/run_analysis.sh

Results will be placed in a `results/` directory.

To reproduce the figures in the publication, follow these steps:

1. Create a `results` directory

2. Use `countwords.py` to count the words in `frankenstein.txt`.

      python bin/countwords.py data/frankenstein.txt --num 100  > 
results/frankenstein.csv

3. Use `plotcounts.py` to plot the resulting file.

      python bin/plotcounts.py

4. Save the plot as `results/frankenstein.pdf`.

5. Edit `bin/countwords.py` and `bin/plotcounts.py` to replace `frankenstein` with 
`dracula`.

6. Repeat the above instructions to generate `dracula.csv` and plot `dracula.pdf`.
