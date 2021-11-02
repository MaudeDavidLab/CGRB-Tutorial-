### InSilicoSeq is a simple command-line tool that allows you to download genomes and create reads with ease.

Installation is simple. You can either use pip or conda.

https://insilicoseq.readthedocs.io/en/latest/iss/install.html#using-pip


Say if you want K genomes of a certain type (bacteria, virus, etc) or you want mixed types, you can use InSilicoSeq to download K random genomes that satisfy your criteria.

You can generate reads in 3 format types:

HiSeq
MiSeq
NovaSeq

### InSilicoSeq can either take a set of genomes to create reads from or you can download genomes to create reads from!

Say we have a genome file `SRS121011.fasta`

If we want to create reads from this specific file we can use the following:

to generate reads in the HiSeq format
```
iss generate --genomes SRS121011.fasta --model hiseq --output hiseq_reads
```
to generate reads in the MiSeq format
```
iss generate --genomes SRS121011.fasta --model miseq --output miseq_reads
```
to generate reads in the NovaSeq format
```
iss generate --genomes SRS121011.fasta --model novaseq --output novaseq_reads
```
Where each call is for each format type for reads

Or say we want to download a few genomes and create MiSeq reads from. This line downloads 10 random bacteria genomes (and saves the full genomes) and generates reads in the MiSeq format.
```
iss generate --ncbi bacteria -u 10 --model miseq --output miseq_ncbi
```

So, to provide a general template:
to generate reads from a given genome file:
```
iss generate --genomes [GENOME_FILE] --model [READ_FORMAT] --output [OUTPUT_FILE_FOR_READS]
```
to generate reads and download genomes:
```
iss generate --genomes -u [NUMBER_OF_GENOMES_YOU_WANT] --model [READ_FORMAT] --output [OUTPUT_FILE_FOR_READS]
```

