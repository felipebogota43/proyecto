# Felipe Bogotá y Sofia Muñoz
# REGULACIÓN TRANSCRIPTÓMICA DE GENES TRANSPORTADORES DE FÓSFORO (PHT1) EN PLANTAS MICORRIZADAS BAJO DEFICIENCIA DE FÓSFORO.

Este pipeline se utilizó en ambos datasets pero para ejemplificar sólo se utilizará el prefijo SRR115 de _Oryza sativa_ y se mostrará cada paso para qué sirvió y cómo se utilizó.


# Descargar secuencias
```
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/039/SRR11540639/SRR11540639_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/039/SRR11540639/SRR11540639_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/040/SRR11540640/SRR11540640_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/040/SRR11540640/SRR11540640_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540642_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540642_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540643/SRR11540643_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540643/SRR11540643_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540644/SRR11540644_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540644/SRR11540644_2.fastq.gz
```
Descargamos las secuencias paired-end de _Oryza sativa_ tanto la forward como la reverse.


# Fatstqc
```fastqc *.fastq.gz```

Con esto se evaluó la calidad de cada secuencia para ver que tanta información correcta y que sea de nuestro estudio de interés poseen y si son adecuadas para trabajar.

# Trimming
Esto sólo se hizo para el SRR115 ya que el SRR682 ya eran secuencias limpias.

```Module load java11

  java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \
  -phred33 \
  SRR11540639_1.fastq.gz SRR11540639_2.fastq.gz \
  R1_paired_39.fastq.gz R1_unpaired_39.fastq.gz \
  R2_paired_39.fastq.gz R2_unpaired_39.fastq.gz \
  ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \
  LEADING:3 TRAILING:3 \
  SLIDINGWINDOW:4:15 \
  MINLEN:36

  java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \
  -phred33 \
  SRR11540640_1.fastq.gz SRR11540640_2.fastq.gz \
  R1_paired_40.fastq.gz R1_unpaired_40.fastq.gz \
  R2_paired_40.fastq.gz R2_unpaired_40.fastq.gz \
  ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \
  LEADING:3 TRAILING:3 \
  SLIDINGWINDOW:4:15 \
  MINLEN:36

  java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \
  -phred33 \
  SRR11540641_1.fastq.gz SRR11540641_2.fastq.gz \
  R1_paired_41.fastq.gz R1_unpaired_41.fastq.gz \
  R2_paired_41.fastq.gz R2_unpaired_41.fastq.gz \
  ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \
  LEADING:3 TRAILING:3 \
  SLIDINGWINDOW:4:15 \
  MINLEN:36

  java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \
  -phred33 \
  SRR11540642_1.fastq.gz SRR11540642_2.fastq.gz \
  R1_paired_42.fastq.gz R1_unpaired_42.fastq.gz \
  R2_paired_42.fastq.gz R2_unpaired_42.fastq.gz \
  ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \
  LEADING:3 TRAILING:3 \
  SLIDINGWINDOW:4:15 \
  MINLEN:36

  java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \
  -phred33 \
  SRR11540643_1.fastq.gz SRR11540643_2.fastq.gz \
  R1_paired_43.fastq.gz R1_unpaired_43.fastq.gz \
  R2_paired_43.fastq.gz R2_unpaired_43.fastq.gz \
  ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \
  LEADING:3 TRAILING:3 \
  SLIDINGWINDOW:4:15 \
  MINLEN:36

  java -jar /opt/ohpc/pub/apps/trimmomatic/0.38/bin/trimmomatic-0.38.jar PE \
  -phred33 \
  SRR11540644_1.fastq.gz SRR11540644_2.fastq.gz \
  R1_paired_44.fastq.gz R1_unpaired_44.fastq.gz \
  R2_paired_44.fastq.gz R2_unpaired_44.fastq.gz \
  ILLUMINACLIP:/opt/ohpc/pub/apps/trimmomatic/0.38/bin/adapters/TruSeq3-PE.fa:2:30:10 \
  LEADING:3 TRAILING:3 \
  SLIDINGWINDOW:4:15 \
  MINLEN:36
```
Con esto hicimos el Trimmomatic y esto ayudó a limpiar las secuencias crudas ya que en el articulo no mencionaban que estuvieran limpias.


# Hisat2
Esta parte usó 2 secuencias en SRR115 porque eran paired-end y en las SRR682 se usó una sola secuencia porque eran single-end.

Antse de cada secuencia se utilizó la ruta de Hisat2: ```/datacnmat01/ciencias/appsbio/conda/envs/appsb/bin/```

```hisat2_extract_splice_sites.py GCA_001433935.1_IRGSP-1.0_genomic.gff > splicesites.tsv
hisat2_extract_exons.py GCA_001433935.1_IRGSP-1.0_genomic.gff > exons.tsv
hisat2-build -p 8 --ss splicesites.tsv --exon exons.tsv GCA_001433935.1.fasta  Rice_index
hisat2 -p 8 -x Rice_index -1 $SRR11540639_1.fastq.gz -2 $SRR11540639_2.fastq.gz -S $SRR11540639.sam
hisat2 -p 8 -x Rice_index -1 $SRR11540640_1.fastq.gz -2 $SRR11540640_2.fastq.gz -S $SRR11540639.sam
hisat2 -p 8 -x Rice_index -1 $SRR11540641_1.fastq.gz -2 $SRR11540641_2.fastq.gz -S $SRR11540639.sam
hisat2 -p 8 -x Rice_index -1 $SRR11540642_1.fastq.gz -2 $SRR11540642_2.fastq.gz -S $SRR11540639.sam
hisat2 -p 8 -x Rice_index -1 $SRR11540643_1.fastq.gz -2 $SRR11540643_2.fastq.gz -S $SRR11540639.sam
```
Con Hisat2 se crearon dos archivo ".tsv",  uno con los exones y otro con los sitios de empalme (splicesites). Luego se usaron esos dos archivos para crear un índice; esto es importante porque los sitios de empalme dan información sobre los saltos de intrones, los exones muestran las regiones codificantes y por último el índice ayuda a agilizar el proceso y que se mapee con precisión las secuencias paired-end.
Hisat2 con el mapeo hace un resumen de todas las lecturas en un solo archivo y esto ayuda a resolver métricas relacionadas con cómo se mapearon y el numero de lecturas.

# Samtools
```module load samtools

for line in $(cat muestras.txt)
do
samtools sort -@ 8 -o $line.bam $line.sam;
done

```
En este "for loop" se cambia de ".sam" a ".bam" ya que no se pude trabajar con ese formato y luego se ordena los productos de ".bam" para que sea mas facil analizarlo después.


  # Htseq-count
  Se utiliz´´o la misma ruta de Histat2 en este proceso
  ```
htseq-count \
    --format=bam \
    --order=pos \
    --mode=intersection-strict \
    --stranded=reverse \
    --minaqual=1 \
    --type=exon \
    --idattr=gene_id \
    "$line.bam" \
   "$GCA_001433935.1_IRGSP-1.0_genomic.gff" \
    > "$line.out"
```

Ya con Htseq-count se cuentan cuantos alineamientos se logran adecuadamente y se logra hacer una matríz en la cual se consigue que todas la secuencias esten en un mismo archivo y que los alineamientos correctos se muestren como un número entero para luego hacer un heatmap.



# Heatmap
```library(edgeR)
library(ggrepel)
library(gplots)
library(RColorBrewer)
library(dplyr)
library(viridis)
x <- read.table("filtered10_counts.tsv", header=T)
row.names(x)<-x$GeneID
x1 <- subset(x, select = -GeneID)
x1[] <- lapply(x1, as.numeric)
x<-as.matrix(x1)
group<-factor(c("AM","AM","NoAM","NoAM","NoAM","AM"))
y<- DGEList(counts=x,group=group)
levels(y$samples$group)
design <- model.matrix(~0+group, data=y$samples)
colnames(design) <- levels(y$samples$group)
y<-calcNormFactors(y)
y<-estimateDisp(y,design)
fit <- glmFit(y, design)
my.contrasts <- makeContrasts(AM_NoAM=AM-NoAM, levels=design)
qlf <- glmLRT(fit, contrast=my.contrasts[,"AM_NoAM"])
summary(decideTests(qlf ,p.value=0.05))
topTags(qlf)
logcounts <- cpm(y,log=TRUE)
var_genes <- apply(logcounts, 1, var)
select_var <- names(sort(var_genes, decreasing=TRUE))[1:100]
highly_variable_lcpm <- logcounts[select_var,]
dim(highly_variable_lcpm)
mypalette <- scale_fill_viridis(discrete = TRUE)
pdf("heatmap.pdf")
heatmap(highly_variable_lcpm,
trace="none",
main="Top 500 most variable genes across samples",
key=TRUE,
scale="row")
dev.off()
```
Con todo esto se creó el hHeatmap que mostraba los genes con alta, intermedia y baja expresión según los colores y también a que tipo de taramiento (micorriza o no micorriza) pertenecía y cuales podrían ser relacionados con el PHT1.
