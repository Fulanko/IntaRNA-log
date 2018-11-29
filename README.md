# IntaRNA-log

## time comparison between master branch and e2int

IntaRNA -t CCCCCCCCGGGGGGGGGGGGGG -q CCCCCCC

| target       | query            | Seed  | time master | time e2int |
|--------------|------------------|-------|------------------| --------------- |
| CCCCCCCCGGGGGGGGGGGGGG     | CCCCCCC   |  Y   | 15ms | 15ms |
| CCCCCCCCGGGGGGGGGGGGGG     | CCCCCCC   |  N   | 15ms | 15ms |
| GCAGCGAGCGAGGACGGCGCAG<br>CGCAGGCGCGACGCGGGCGCGCGCG | CGCGCGCGGGCCGCGCGCGCG<br>CGCGCGCGGCCGCGGCGACGAG<br>GCAGGCGCACGGCACGGCA | Y | 62ms | 67ms |
| GCAGCGAGCGAGGACGGCGCAG<br>CGCAGGCGCGACGCGGGCGCGCGCG | CGCGCGCGGGCCGCGCGCGCG<br>CGCGCGCGGCCGCGGCGACGAG<br>GCAGGCGCACGGCACGGCA | N | 52ms | 55ms |
| CCCCCCCCCCCCCCCCCCCCCC<br>CCCCCCCCCCCCCCCC | GGGGGGGGGGGGGGGGGGG<br>GGGGGGGGGGGGGGGGGGGG | Y | 119ms | 119ms |
| CCCCCCCCCCCCCCCCCCCCCC<br>CCCCCCCCCCCCCCCC | GGGGGGGGGGGGGGGGGGG<br>GGGGGGGGGGGGGGGGGGGG | N | 81ms | 78ms |
| ACGGCGAGCGGCAGCAGACGGC<br>GGCACGACGACGACGACGACGG<br>CGAGCGCACGAGACCGACGCAG<br>GCACGGACGACGACGACGACCGAGCAGACG | CGACGAGCAGAGCGACGGCAGC<br>AGCCGAGCAGACCGAACGGCAC<br>GGCGCGCAGCAGACGACGCAAG<br>GCGCAGCAGCAGCAGCGCGCGA<br>GACGGGCAGCAGCAGCAGCAGC<br>GCGACGCGCAGCACGAGCAGCCGAAGC | N | 150ms | 156ms |
