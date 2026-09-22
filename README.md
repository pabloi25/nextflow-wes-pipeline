# nextflow-wes-pipeline

Reproducible WES variant calling pipeline from FASTQ to filtered VCF using Nextflow and GATK.

## Overview

This repository contains a modular Nextflow workflow for whole-exome sequencing (WES) data processing and germline variant calling.

The project is being developed step by step, with an emphasis on:

- reproducibility
- modular workflow design
- transparent quality control
- clear parameterization
- practical troubleshooting
- validation against established workflows

## Planned workflow

```text
FASTQ
  ↓
FastQC
  ↓
fastp
  ↓
FastQC (post-trimming)
  ↓
BWA-MEM
  ↓
SAM/BAM processing
  ↓
MarkDuplicates
  ↓
BQSR
  ↓
GATK HaplotypeCaller
  ↓
GenotypeGVCFs
  ↓
VariantFiltration
  ↓
Filtered VCF
```

## Development status

The pipeline is currently under active development.

### Phase 1 — Read preprocessing

- [ ] FastQC on raw reads
- [ ] fastp trimming
- [ ] FastQC on trimmed reads

### Phase 2 — Alignment and BAM processing

- [ ] BWA-MEM alignment
- [ ] BAM sorting and indexing
- [ ] Duplicate marking
- [ ] Alignment QC

### Phase 3 — Variant calling

- [ ] Base Quality Score Recalibration (BQSR)
- [ ] GATK HaplotypeCaller
- [ ] GenotypeGVCFs
- [ ] Variant filtration

### Phase 4 — Reproducibility and validation

- [ ] Multi-sample support
- [ ] Conda environments
- [ ] Test dataset
- [ ] MultiQC reporting
- [ ] Benchmarking against nf-core/sarek

## Technologies

- Nextflow
- GATK
- BWA
- SAMtools
- Picard
- FastQC
- fastp
- MultiQC

## Intended use

This project is intended for educational, research, workflow-development and portfolio purposes.

It is not intended for direct clinical diagnostic use without appropriate validation, quality management and regulatory oversight.

## Data privacy

No patient FASTQ, BAM, CRAM, VCF or personally identifiable genomic data should be committed to this repository.

Public or synthetic test data will be used for workflow testing and examples.

## Author

Pablo F. Isa

Genetics and bioinformatics — WES, NGS workflows and variant analysis.
