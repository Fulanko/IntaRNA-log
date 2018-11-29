# IntaRNA-log

## time comparison between master branch and e2int

IntaRNA -t CCCCCCCCGGGGGGGGGGGGGG -q CCCCCCC

| target       | query            | Seed  | time master | time e2int |
|--------------|------------------|-------|------------------| --------------- |
| CCCCCCCCGGGGGGGGGGGGGG     | CCCCCCC   |  Y   | 15ms | 15ms |
| CCCCCCCCGGGGGGGGGGGGGG     | CCCCCCC   |  N   | 15ms | 15ms |
| GCAGCGAGCGAGGACGGCGCAGCGCAGGCGCGACGCGGGCGCGCGCG | CGCGCGCGGGCCGCGCGCGCGCGCGCGCGGCCGCGGCGACGAGGCAGGCGCACGGCACGGCA | Y | 62ms | 67ms |
| GCAGCGAGCGAGGACGGCGCAGCGCAGGCGCGACGCGGGCGCGCGCG | CGCGCGCGGGCCGCGCGCGCGCGCGCGCGGCCGCGGCGACGAGGCAGGCGCACGGCACGGCA | N | 52ms | 55ms |
| CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC | GGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGG | Y | 119ms | 119ms |
| CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC | GGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGG | N | 81ms | 78ms |
| ACGGCGAGCGGCAGCAGACGGCGGCACGACGACGACGACGACGGCGAGCGCACGAGACCGACGCAGGCACGGACGACGACGACGACCGAGCAGACG | CGACGAGCAGAGCGACGGCAGCAGCCGAGCAGACCGAACGGCACGGCGCGCAGCAGACGACGCAAGGCGCAGCAGCAGCAGCGCGCGAGACGGGCAGCAGCAGCAGCAGCGCGACGCGCAGCACGAGCAGCCGAAGC | N | 150ms | 156ms |
