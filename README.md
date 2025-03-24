# NanoporeLong5
Script takes Fastq file and POD5 (all reads in fastq need to be in POD5 data), combinning the data from both, and creates a long5 file with signal, dwell time, nucleotides, phred score, PolyA classification.  The data format is such that each point of signal from the nanopore is a diffrent row, in pA units.

**The actual file you want to use for analyses is named: combined_merged_signal_fastq_sequences_ready.long5**


*The Slow5-Dorado script has a "Oxford Nanopore Technologies PLC. Public License Version 1.0", you must adhere to this license as well.


**Format of the file:**

sequence_name= read name

nucleotide_index = nucleotide index in fastq if it was read 5'->3'

phred_score=nucleotide phred score as its in the fastq

dwell_time = dwell time for the nucleotide

time = time measurment for the signal, ie 0 being the start of reading the read through the nanopore.

signal= signal in pA

signal_index = index of the signal measurment

plotted_nucleotide = nucleotide index in the fastq if it was read 5' -> 3'

sequence_type_plotted= what is the region type, it is assuming its RNA after PolyA





----------------------------------------------------------------------------------------------------------------------------------------------

****Install:****

git clone https://github.com/haimkru/NanoporeLong5.git

cd NanoporeLong5

tar -xvf NanoporeLong5.tar

sh installation.sh

* You need to run the installtion Command only once, it might request permissions to download packages such as Rscript, please do y to permit the installation of the dependencies

----------------------------------------------------------------------------------------------------------------------------------------------





**To Run Program**

**Notes For Running**
1. Less reads = Will run faster
  
2. If POD5 file contains less reads = Runs faster, as re-basecalling is performed on the entire POD5 file. but! we nonetheless filter our reads so its not a big diffrence
  
3. Script creates alot of temporary files, in reallity only file that is needed is the final file : combined_merged_signal_fastq_sequences_ready.long5, feel free to delete all the temporary files as they are mainly for QC incase there are problems mid run.



**Then to run you do:**

**bash From_fastq_pod5_predict_RNA_for_github.sh  <input.fastq> <input.pod5> <output_directory> <N_threads> <directory_of_scripts>"**



input fastq= Fastq file with the reads we want to process

input pod5 = POD5 file that cotnains all the reads from Fastq

output directory = The directory we want our long5 and temporary files will be the output

N_threads = Number of threads for running our long5 convertor

directory_of_scripts = The directory in which we installed NanoporeLong5 scripts 

----------------------------------------------------------------------------------------------------------------------------------------------

**Example plotting in R is found in the Rscript file: example_plotting_a_single_read.R**

----------------------------------------------------------------------------------------------------------------------------------------------


**For Example:**

bash /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_RNA_analysis_up_to_plotting/All_scripts_for_github_upload/From_fastq_pod5_predict_RNA_for_github.sh /media/data2/hkrupkin/nanopore/detecting_RNA/My_own_nanopore_run/sequencing_run_nanopore/all_fastq_files_uncompressed_top100_reads.fastq /media/data2/hkrupkin/nanopore/detecting_RNA/My_own_nanopore_run/sequencing_run_nanopore/pod_5_files_all/all_pod5_files/merged.pod5 /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_RNA_analysis_up_to_plotting/Finding_RNAs_by_Kmer/Test_run_examination_entire_file_v5_100_reads 20 /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_RNA_analysis_up_to_plotting/All_scripts_for_github_upload




**for problems with code please feel free to either leave an issue request in the github page, or email me at hkrupkin@stanford.edu**





