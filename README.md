# proyecto
Proyecto bioinfo


# Paso1

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/039/SRR11540639/SRR11540639_1.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/039/SRR11540639/SRR11540639_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/040/SRR11540640/SRR11540640_1.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/040/SRR11540640/SRR11540640_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_1.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540642_1.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540642_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540643/SRR11540643_1.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540643/SRR11540643_2.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540644/SRR11540644_1.fastq.gz```

```wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540644/SRR11540644_2.fastq.gz```

Descaragmos las secuencias paired-end de oryza sativa tanto la forward como la reverse


# Paso2
```Module load java11```


```java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \```
```-phred33 \```
```SRR11540639_1.fastq.gz SRR11540639_2.fastq.gz \```
```R1_paired_39.fastq.gz R1_unpaired_39.fastq.gz \```
```R2_paired_39.fastq.gz R2_unpaired_39.fastq.gz \```
```ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \```
```LEADING:3 TRAILING:3 \```
```SLIDINGWINDOW:4:15 \```
```MINLEN:36```

```java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \```
```-phred33 \```
```SRR11540640_1.fastq.gz SRR11540640_2.fastq.gz \```
```R1_paired_40.fastq.gz R1_unpaired_40.fastq.gz \```
```R2_paired_40.fastq.gz R2_unpaired_40.fastq.gz \```
```ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \```
```LEADING:3 TRAILING:3 \```
```SLIDINGWINDOW:4:15 \```
```MINLEN:36```

```java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \```
```-phred33 \```
```SRR11540641_1.fastq.gz SRR11540641_2.fastq.gz \```
```R1_paired_41.fastq.gz R1_unpaired_41.fastq.gz \```
```R2_paired_41.fastq.gz R2_unpaired_41.fastq.gz \```
```ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \```
```LEADING:3 TRAILING:3 \```
```SLIDINGWINDOW:4:15 \```
```MINLEN:36```

```java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \```
```-phred33 \```
```SRR11540642_1.fastq.gz SRR11540642_2.fastq.gz \```
```R1_paired_42.fastq.gz R1_unpaired_42.fastq.gz \```
```R2_paired_42.fastq.gz R2_unpaired_42.fastq.gz \```
```ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \```
```LEADING:3 TRAILING:3 \```
```SLIDINGWINDOW:4:15 \```
```MINLEN:36```

```java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \```
```-phred33 \```
```SRR11540643_1.fastq.gz SRR11540643_2.fastq.gz \```
```R1_paired_43.fastq.gz R1_unpaired_43.fastq.gz \```
```R2_paired_43.fastq.gz R2_unpaired_43.fastq.gz \```
```ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \```
```LEADING:3 TRAILING:3 \```
```SLIDINGWINDOW:4:15 \```
```MINLEN:36```

```java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \```
```-phred33 \```
```SRR11540644_1.fastq.gz SRR11540644_2.fastq.gz \```
```R1_paired_44.fastq.gz R1_unpaired_44.fastq.gz \```
```R2_paired_44.fastq.gz R2_unpaired_44.fastq.gz \```
```ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \```
```LEADING:3 TRAILING:3 \```
```SLIDINGWINDOW:4:15 \```
```MINLEN:36```


Con esto hicimos el Trimmomatic y esto ayudo a limpiar las secuencias crudas ya que en el articulo no mencionaban que estuvieran limpias.

# Paso3
```fastqc *.fastq.gz```

  Con esto se evalua la calidad de cada secuencia par ver que tanta informacion correcta y que sea de nustro estidio de interes poseen y si son adecuadas para trabajar.

# Paso4
```hisat2_extract_splice_sites.py GCA_001433935.1_IRGSP-1.0_genomic.gff > splicesites.tsv```

```hisat2_extract_exons.py GCA_001433935.1_IRGSP-1.0_genomic.gff > exons.tsv```

```hisat2-build -p 8 --ss splicesites.tsv --exon exons.tsv GCA_001433935.1.fasta  Rice_index```

Con hisat2 se crean dos.tsv  uno con los exones y otro con los sitios de empalme(splicesites)luego se usa eso dos atchivos para crear un indice  esto es importante porque los istios de mepalme dan información sobre los saltos de intrones,los exones muestran las regines codificantes y por ultimo el indice a agilizar el proceso y que se mapee con precision las secuencias paired-end.

# Paso5
```hisat2 -p 8 -x Rice_index -1 $SRR11540639_1.fastq.gz -2 $SRR11540639_2.fastq.gz -S $SRR11540639.sam```
```hisat2 -p 8 -x Rice_index -1 $SRR11540640_1.fastq.gz -2 $SRR11540640_2.fastq.gz -S $SRR11540639.sam```
```hisat2 -p 8 -x Rice_index -1 $SRR11540641_1.fastq.gz -2 $SRR11540641_2.fastq.gz -S $SRR11540639.sam```
```hisat2 -p 8 -x Rice_index -1 $SRR11540642_1.fastq.gz -2 $SRR11540642_2.fastq.gz -S $SRR11540639.sam```
```hisat2 -p 8 -x Rice_index -1 $SRR11540643_1.fastq.gz -2 $SRR11540643_2.fastq.gz -S $SRR11540639.sam```

Hisat2 con el mapeo hace un resumen de todas las lecturas en un solo archivo y esto ayuda a resolver metricas relacionadas con como se mapearon y el numero de lecturas.

# Paso6
```` module load samtools```
```for line in SRR11540639 SRR11540640 SRR11540641 SRR11540642 SRR11540643 SRR11540644; do```
  ```sam="${line}.sam"```
  ```bam="${line}.bam"```
  
  ```samtools sort -@ 8 -o "${line}.bam" "${line}.sam"```

