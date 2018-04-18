# LOCOM
Closed gradual and exceptional patterns miner.

To be able to compile the code it will be necessary to install the library boost on its machine,

for this it will follow the following instructions:

1 - Download boost of this link: http://sourceforge.net/project/showfiles.php?group_id=7586&package_id=8041
2 - On the installation folder of boost it will be necessary to execute the following instruction:
tar --bzip2 -xf /path/to/boost_1_45_0.tar.bz2
3 - To compile with boost it will be necessary to install it in the directory include


It will be necessary to execute the make file by going in the folder where the code is located and to type: make

* In Gradualpattern_Exceptional_mining / => Gradual extractor exceptional patterns 
 
A,B,C,D,E,F ==> Attributs 
S,N,S,G,G,G ==> for description (Symbolic "S" and/or Numeric "N"), G: it is for gradual attributes
A,1,4,1,1,2
D,2,4,2,2,4
A,5,4,3,2,12
S,1,3,4,2,10
D,2,3,1,2,6
 
--- Command ---

Arguments: -G: Threshold for gradual pattern support (on the entire dataset)
-d: Threshold for the support of the description (support on the description "d")
-g: Threshold for support g on description "d"

Example: ./ExcepGrad toy.txt Transformed.DATA -g 0.4 -d 0.01 -G 0.3

If we do not specify anything as arguments the supports are considered to be 0.

The output is a csv file; example of result for the gradual attribute F:

./ExcepGrad jouet.txt Transformed.DATA -G 0.1 -d 0.3 -g 0.1 -w 0.01
check the output.csv file

 
