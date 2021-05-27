# ProtExcluder

This version works with new Diamond / Blast output. Make sure to set outfmt 0 for both aligners.

This is a modified version of ProtExcluder downloaded from its original site at
http://www.hrt.msu.edu/uploads/535/78637/ProtExcluder1.2.tar.gz

Two of the scripts, namely `ProtExcluder.npl` and `mspesl-sfetch.npl` are
modified so that the paths for HMMER and this package do not need to be changed
after conda install. 

For any potential questions regarding running the software, please refer to the
original webpage at
http://weatherby.genetics.utah.edu/MAKER/wiki/index.php/Repeat_Library_Construction-Advanced


==

Nanjiang Shu (NBIS)
nanjiang.shu@nbis.se

Install instruction:
git clone https://github.com/qisun2/ProtExcluder.git
cd ProtExcluder

#make sure to use hmmer version with binaries/esl-* files under the hmmer direcytory
./Installer.pl -m /path/to/hmmer-3.1b1 -p /install/target/path/ProtExcluder

cd ..

cp -r ProtExcluder /install/target/path/

#run the code as :
/install/target/path/ProtExcluder/ProtExcluder.pl blastout.txt sequence.fasta

#Note: blastout.txt was generated with "diamond blastx --outfmt 0 <other options>"
