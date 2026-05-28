# proyecto
Proyecto bioinfo


# paso1
'''wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/039/SRR11540639/SRR11540639_1.fastq.gz'''
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/039/SRR11540639/SRR11540639_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/040/SRR11540640/SRR11540640_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/040/SRR11540640/SRR11540640_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/041/SRR11540641/SRR11540641_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540642_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540642_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540643_1.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540643_2.fastq.gz
wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540644_1.fastq.gz
wgte ftp.sra.ebi.ac.uk/vol1/fastq/SRR115/042/SRR11540642/SRR11540644_2.fastq.gz

Con esto descargamos el paired - end de las secuencias de oryza sativa tanto la reverse como la forward
# paso2
Module load java11

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
R2_paired_39.fastq.gz R2_unpaired_41.fastq.gz \
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

Con esto hicimos el Trimmomatic y esto ayudo a limpiar las secuencias crudas ya que en el articulo no mencionaban que estuvieran limpias.

# Paso3
fastqc*.fastq.gz
con esto se evalua la calidad de cada secuencia

# Paso4

