# NanoporeLong5
Script takes Fastq file and POD5 (all reads in fastq need to be in POD5 data), combinning the data from both, and creates a long5 file with signal, dwell time, nucleotides, phred score, PolyA classification.  The data format is such that each point of signal from the nanopore is a diffrent row, in pA units.






The Slow5-Dorado script has a "Oxford Nanopore Technologies PLC. Public License Version 1.0", you must adhere to this license as well, thus, this script "NanoporeLong5" can only be used for research purposes

----------------------------------------------------------------------------------------------------------------------------------------------

****Install:****

**git install**

wget 

----------------------------------------------------------------------------------------------------------------------------------------------

**To Run Program**

**Notes For Running**
1. Less reads = Will run faster
  
3. If POD5 file contains less reads = Runs faster, as re-basecalling is performed on the entire POD5 file.
  
4. Creates alot of temporary files, in reallity only file that is needed is the final file : combined_merged_signal_fastq_sequences_ready.long5, feel free to delete all the temporary files as they are mainly for QC in case there are problems mid run.

**first we run the script for installing everything**

sh /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_DragonRNA_analysis_up_to_plotting/All_scripts_for_github_upload/installation.sh

**Then to run you do:**

bash From_fastq_pod5_predict_DragonRNA_for_github.sh  <input.fastq> <input.pod5> <output_directory> <N_threads> <directory_of_scripts>"

**For Example:**

bash /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_DragonRNA_analysis_up_to_plotting/All_scripts_for_github_upload/From_fastq_pod5_predict_DragonRNA_for_github.sh /media/data2/hkrupkin/nanopore/detecting_dragonRNA/My_own_nanopore_run/sequencing_run_nanopore/all_fastq_files_uncompressed_top100_reads.fastq /media/data2/hkrupkin/nanopore/detecting_dragonRNA/My_own_nanopore_run/sequencing_run_nanopore/pod_5_files_all/all_pod5_files/merged.pod5 /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_DragonRNA_analysis_up_to_plotting/Finding_RNAs_by_Kmer/Test_run_examination_entire_file_v5_100_reads 20 /media/data2/hkrupkin/code/nanopore_related/Custom_code/Single_Script_all_DragonRNA_analysis_up_to_plotting/All_scripts_for_github_upload









