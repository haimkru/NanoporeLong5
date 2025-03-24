# NanoporeLong5
Script takes Fastq file and POD5 (all reads in fastq need to be in POD5 data), combinning the data from both, and creates a long5 file with signal, dwell time, nucleotides, phred score, PolyA classification.  The data format is such that each point of signal from the nanopore is a diffrent row, in pA units.

The Slow5-Dorado script has a "Oxford Nanopore Technologies PLC. Public License Version 1.0", you must adhere to this license as well, thus, this script "NanoporeLong5" can only be used for research purposes

**Install:**


**First We Install blue-crab**

pip install blue-crab

blue-crab --help


**Then we Install slow5 dorado**

wget https://github.com/hiruna72/slow5-dorado/releases/download/v0.8.3/slow5-dorado-v0.8.3-x86_64-linux.tar.xz -O slow5-dorado.tar.xz

tar xf slow5-dorado.tar.xz

cd slow5-dorado/bin

./slow5-dorado --version

**we also need to install the correct slow5 dorado model, currently its set to the RNA model for RNA004**
But this code can be changed, to another model, just download the other model, and in the file From_fastq_pod5_predict_DragonRNA_for_github.sh change the row 63 the model used to the correct model


./slow5-dorado download --model rna004_130bps_sup@v3.0.1

**Then we Install squigualiser**

wget https://github.com/hiruna72/squigualiser/releases/download/v0.6.3/squigualiser-v0.6.3-linux-x86-64-binaries.tar.gz -O squigualiser.tar.gz

tar xf squigualiser.tar.gz

cd squigualiser

./squigualiser --help






