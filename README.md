# NanoporeLong5
Script takes Fastq file and POD5 (all reads in fastq need to be in POD5 data), combinning the data from both, and creates a long5 file with signal, dwell time, nucleotides, phred score, PolyA classification.  The data format is such that each point of signal from the nanopore is a diffrent row, in pA units.

The Slow5-Dorado script has a "Oxford Nanopore Technologies PLC. Public License Version 1.0", you must adhere to this license as well, thus, this script "NanoporeLong5" can only be used for research purposes

**Install:**


**First We Install blue-crab**
pip install blue-crab
blue-crab --help

**Then we Install slow5 dorado**
wget https://github.com/hiruna72/slow5-dorado/releases/download/v0.8.2/slow5-dorado-v0.8.2-x86_64-linux.tar.gz -O slow5-dorado.tar.gz
tar xf slow5-dorado.tar.gz
cd slow5-dorado/bin
./slow5-dorado --version






