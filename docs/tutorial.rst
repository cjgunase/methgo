Tutorial
========

1. Download the sample input file

  ::

  $ curl -O http://paoyang.ipmb.sinica.edu.tw/public_data/methgo_demo.tar.gz
  $ tar xvfz methgo_demo.tar.gz
  $ cd methgo_demo/data

2. Run COV module:

  ::

  $ methgo cov genome.fa demo.CGmap

  .. image:: _static/demo.cov.png

3. Run MET module:

  ::

  $ methgo met genes.gtf genome.fa demo.CGmap

  .. image:: _static/demo.bulk.hist.png
  .. image:: _static/demo.bulk.mean.png
  .. image:: _static/demo.feature.CG.png
  .. image:: _static/demo.feature.CHG.png
  .. image:: _static/demo.feature.CHH.png
  .. image:: _static/demo.genomewide.png

4. Run TXN module:

  ::

  $ methgo txn -t methgo/scripts/txn/tair10_txn -l ATHB1_binding_site_motif,CCA1_binding_site_motif -c demo.CGmap

  .. image:: _static/demo.CG.txn.png
  .. image:: _static/demo.CHG.txn.png
  .. image:: _static/demo.CHH.txn.png

5. Run SNP module:

  ::

  $ methgo snp -g genome.fa demo.sorted.bam

6. Run CNV module:

  ::

  $ methgo cnv genome.fa.fai demo.sorted.bam

  .. image:: _static/demo.sorted.cnv.png
