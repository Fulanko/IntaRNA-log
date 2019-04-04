# Plots

## Exact, memory-efficient length-dependent
[Performance](./plots/exact_length.pdf)  
[Runtime](./plots/exact_length_runtime.pdf)  
[Memory](./plots/exact_length_memory.pdf)  

## Heuristic length-dependent
[Performance](./plots/heuristic_length.pdf)  
[Runtime](./plots/heuristic_length_runtime.pdf)  
[Memory](./plots/heuristic_length_memory.pdf)  

## Riblast length-dependent
[Performance](./plots/riblast_length.pdf)  
[Runtime](./plots/riblast_length_runtime.pdf)  
[Memory](./plots/riblast_length_memory.pdf)  

## Data generation script

```[bash]
#########################################################################

# benchmark on new cluster with qsub in
# /scratch/bi03/gelhausr/intaRNA/IntaRNA-benchmark/

# results in
# /scratch/bi03/gelhausr/intaRNA/IntaRNA-benchmark/benchmark-Frank/

#########################################################################

# use all threads
defaultArgs=""

IntaRNA="/scratch/rna/bisge001/Software/intarna/dev-Frank-190403/bin/IntaRNA"

#########################################################################

function printCall {
echo "qsub -pe smp 24 -o /scratch/bi03/gelhausr/intaRNA/IntaRNA-benchmark/sge-out/ intarna-benchmark-sge.sh -e -b $IntaRNA -c '$1' -o './benchmark-Frank/' -a '$2 $defaultArgs'";
} 

function printCallNewED {
echo "qsub -pe smp 24 -o /scratch/bi03/gelhausr/intaRNA/IntaRNA-benchmark/sge-out/ intarna-benchmark-sge.sh -b $IntaRNA -c '$1' -o './benchmark-Frank/' -a '$2 $defaultArgs'";
} 

#########################################################################
# calls 190403
#########################################################################
(

# master default
#printCall "default" " --threads=0"
#printCallNewED "mem-default" " --threads=1 --tacc=N --qacc=N"

intLenMax="20 30 40 50 60 70 80 100"

# need to recompute EDs, since otherwise --tIntLenMax is set by calls.py
for l in $intLenMax; do 
# master short interactions
# printCall "default-intLenMax$l" " --qIntLenMax=$l --tIntLenMax=$l --threads=0"
# printCallNewED "mem-default-intLenMax$l" " --qIntLenMax=$l --tIntLenMax=$l --threads=1 --tacc=N --qacc=N"
# seed-extension
for m in M H R; do
printCall "X-$m-intLenMax$l" " --model=X -m $m --qIntLenMax=$l --tIntLenMax=$l --threads=0"
#  printCallNewED "mem-X-$m-intLenMax$l" " --model=X -m $m --qIntLenMax=$l --tIntLenMax=$l --threads=1 --tacc=N --qacc=N"
done
# for m in M H; do
#  printCall "E-$m-intLenMax$l" " --model=E -m $m --qIntLenMax=$l --tIntLenMax=$l --threads=0"
#  printCallNewED "mem-E-$m-intLenMax$l" " --model=E -m $m --qIntLenMax=$l --tIntLenMax=$l --threads=1 --tacc=N --qacc=N"
# done
done


) > calls.190403.sh # | sort
#########################################################################
```
