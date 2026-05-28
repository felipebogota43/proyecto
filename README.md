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
```module load samtools```

```for line in SRR11540639 SRR11540640 SRR11540641 SRR11540642 SRR11540643 SRR11540644```
```do```

  ```sam="$SRR11540639.sam"```
  
  ```bam="$SRR11540639.bam"```
  
  ```samtools sort -@ 8 -o "$SRR11540639.bam" "$SRR11540639.sam"```
  En este for loop se cambia de sam a bam ya que no se pude trabajar con ese formato y luego se ordena los productos de bam par que sea mas facil analizarlo despues

  # Paso7
```htseq-count \```
    ```--format=bam \```
    ```--order=pos \```
    ```--mode=intersection-strict \```
    ```--stranded=reverse \```
    ```--minaqual=1 \```
    ```--type=exon \```
    ```--idattr=gene_id \```
    ```"$bam" \```
    ```"$GCA_001433935.1_IRGSP-1.0_genomic.gff" \```
    ```> "$out"```
    Ya con htseq-count se cuentan cuantos alineamientos se logran adecuadamente y se logra hacer una matriz en la cual se consigue que todas la secuencias esten en un mismo archivo y que los alineamientos corrrectos se mueatren ea un numero entero para luego hacer un heatmap.

# Paso8
```library(edgeR)```
```library(ggrepel)```
```library(gplots)```
```library(RColorBrewer)```
```library(dplyr)```
```library(viridis)```

```x <- read.table("filtered10_counts.tsv", header=T)```

```row.names(x)<-x$GeneID```

```x1 <- subset(x, select = -GeneID)```

```x1[] <- lapply(x1, as.numeric)```

```x<-as.matrix(x1)```

```group<-factor(c("AM","AM","NoAM","NoAM","NoAM","AM"))```

```y<- DGEList(counts=x,group=group)```

```levels(y$samples$group)```

```design <- model.matrix(~0+group, data=y$samples)```

```colnames(design) <- levels(y$samples$group)```

```y<-calcNormFactors(y)```

```y<-estimateDisp(y,design)```

```fit <- glmFit(y, design)```

```my.contrasts <- makeContrasts(AM_NoAM=AM-NoAM, levels=design)```

```qlf <- glmLRT(fit, contrast=my.contrasts[,"AM_NoAM"])```

```summary(decideTests(qlf ,p.value=0.05))```

```topTags(qlf)```

```logcounts <- cpm(y,log=TRUE)```

```var_genes <- apply(logcounts, 1, var)```

```select_var <- names(sort(var_genes, decreasing=TRUE))[1:100]```

```highly_variable_lcpm <- logcounts[select_var,]```

```dim(highly_variable_lcpm)```

```mypalette <- scale_fill_viridis(discrete = TRUE)```

```pdf("heatmap.pdf")```

```heatmap.2(highly_variable_lcpm,```
```trace="none",```
```main="Top 500 most variable genes across samples",```
```key=TRUE,```
```scale="row")```
```dev.off()```
Con todo esto se creo el heatmap que mostraba los genes con alta,intermedia y baja expresion segun los colores y tambien a que tipo de planta micorriza o no micorriza pertenecia y cuales podian ser relacionados con el PHT1.

dev.off()
