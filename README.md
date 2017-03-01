# hercules-v.1.0
Homology Evidence RNA-seq CDS predictor



Author: Guo qingxiang

Email: guoqing@webmail.hzau.edu.cn

Released: 2017-03-1

(H)omology (E)vidence (R)NA-seq (C)DS rules

Hercules enables you to predict CDS from RNA-seq transcripts from homology evidence.

You can give Hercules four blast result files (in outfmt6).

Hercules will combine it with customed priority and produce a gene-call file which can be fed into Anvi'o.

After get the gene-call file:

First, type

anvi-gen-contigs-database -f contigs.fa -o contigs.db --external-gene-calls gene_call

then, to get CDS:

anvi-get-dna-sequences-for-gene-calls -c contigs.db -o CDS.fa

to get protein sequence:

anvi-get-aa-sequences-for-gene-calls -c contigs.db -o aa.fa

For information about anvi'o, see:

http://merenlab.org/2016/06/26/installation-v2/

