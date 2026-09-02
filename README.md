# xcParTurq1.1

This repository contains the workflows that were used to assemble the genome
xcParTurq1.1 for *Pareledone turqueti*.

The repo was produced automatically from boilerplate code at
[AToL-Bioinformatics/genome-launcher-workflow](https://github.com/AToL-Bioinformatics/genome-launcher-workflow).

### Assembly data

<details>

<summary>Click to view YAML</summary>

```yaml
assembly_id: 4868f56a-c3b6-49b7-9ad8-d3fb04daa3f7
assembly_version: 1
augustus_dataset_name: Notospermus_geniculatus
busco_odb10_dataset_name: mollusca
busco_odb12_dataset_name: mollusca
dataset_id: xcParTurq1
genetic_code_id: 1
hic_motif: GATC,GANTC,CTNAG,TTAA
mitochondrial_genetic_code_id: 5
mitohifi_reference_species: Octopus vulgaris
ncbi_class: Cephalopoda
oatk_hmm_name: mollusca
read_files:
- base_url: https://downloads-qcif.bioplatforms.com/bpa/avid_staging/pacbio-hifi/BPAOPS-2187/20260817_AVID_AGRF_CAGRF26040069_m84073_260813_074149_s2/
  data_type: PACBIO_SMRT
  name: bpa-avid-pacbio-hifi-668779-m84073_260813_074149_s2
  single_end:
  - md5sum: 81b821d3f2f89a2032ff81b0655d6232
    url: https://data.bioplatforms.com/dataset/bpa-avid-pacbio-hifi-668779-m84073_260813_074149_s2/resource/81b821d3f2f89a2032ff81b0655d6232/download/668779_AVID_AGRF_m84073_260813_074149_s2.ccs.bam
- base_url: https://downloads-qcif.bioplatforms.com/bpa/avid_staging/pacbio-hifi/BPAOPS-2185/20260817_AVID_AGRF_CAGRF26040069_m84073_260714_071431_s1/
  data_type: PACBIO_SMRT
  name: bpa-avid-pacbio-hifi-668779-m84073_260714_071431_s1
  single_end:
  - md5sum: f1ff80f636e1c7d97bcaca3861714581
    url: https://data.bioplatforms.com/dataset/bpa-avid-pacbio-hifi-668779-m84073_260714_071431_s1/resource/f1ff80f636e1c7d97bcaca3861714581/download/668779_AVID_AGRF_m84073_260714_071431_s1.ccs.bam
- base_url: https://downloads-qcif.bioplatforms.com/bpa/avid_staging/pacbio-hifi/BPAOPS-2183/20260817_AVID_AGRF_CAGRF26040069_m84073_260601_035615_s4/
  data_type: PACBIO_SMRT
  name: bpa-avid-pacbio-hifi-668779-m84073_260601_035615_s4
  single_end:
  - md5sum: 67d6e1becc5ec571d532cd3db38fffb1
    url: https://data.bioplatforms.com/dataset/bpa-avid-pacbio-hifi-668779-m84073_260601_035615_s4/resource/67d6e1becc5ec571d532cd3db38fffb1/download/668779_AVID_AGRF_m84073_260601_035615_s4.ccs.bam
- base_url: https://downloads-qcif.bioplatforms.com/bpa/avid_staging/pacbio-hifi/BPAOPS-2186/20260817_AVID_AGRF_CAGRF26040069_m84073_260813_070932_s1/
  data_type: PACBIO_SMRT
  name: bpa-avid-pacbio-hifi-668779-m84073_260813_070932_s1
  single_end:
  - md5sum: 213108f7691e25105a9baad8fb538ed2
    url: https://data.bioplatforms.com/dataset/bpa-avid-pacbio-hifi-668779-m84073_260813_070932_s1/resource/213108f7691e25105a9baad8fb538ed2/download/668779_AVID_AGRF_m84073_260813_070932_s1.ccs.bam
- base_url: https://downloads-qcif.bioplatforms.com/bpa/avid_staging/pacbio-hifi/BPAOPS-2184/20260817_AVID_AGRF_CAGRF26040069_m84073_260708_083233_s3/
  data_type: PACBIO_SMRT
  name: bpa-avid-pacbio-hifi-668779-m84073_260708_083233_s3
  single_end:
  - md5sum: eb94647fbd47a826cd18f2db271bf2d4
    url: https://data.bioplatforms.com/dataset/bpa-avid-pacbio-hifi-668779-m84073_260708_083233_s3/resource/eb94647fbd47a826cd18f2db271bf2d4/download/668779_AVID_AGRF_m84073_260708_083233_s3.ccs.bam
- base_url: https://downloads-qcif.bioplatforms.com/bpa/avid_staging/illumina-shortread/BPAOPS-2107/20260605_AVID_BRF_WO31004_23JG5LLT3/
  data_type: Hi-C
  name: bpa-avid-illumina-shortread-668783-23jg5llt3
  r1:
  - md5sum: c3cebedaaf3ccd6e4d804eed857a7ab0
    url: https://data.bioplatforms.com/dataset/bpa-avid-illumina-shortread-668783-23jg5llt3/resource/c3cebedaaf3ccd6e4d804eed857a7ab0/download/668783_AVID_BRF_23JG5LLT3_TGAGGAGT-CGCGCAAT_S19_R1_001.fastq.gz
  r2:
  - md5sum: 5740c1289898cbf18e70df52af0c2553
    url: https://data.bioplatforms.com/dataset/bpa-avid-illumina-shortread-668783-23jg5llt3/resource/5740c1289898cbf18e70df52af0c2553/download/668783_AVID_BRF_23JG5LLT3_TGAGGAGT-CGCGCAAT_S19_R2_001.fastq.gz
scientific_name: Pareledone turqueti
taxon_id: 164545

```

</details>

## Overview

The assembly process has three main steps:

1. Assembly with
   [sanger-tol/genomeassembly](https://github.com/sanger-tol/genomeassembly/)
2. Decontamination with [sanger-tol/ascc](https://github.com/sanger-tol/ascc/)
3. Preparation of curation materials with
   [sanger-tol/treeval](https://github.com/sanger-tol/treeval/), if there are
   Hi-C reads.

The config files for these steps are in the [config](./config) directory.

The sanger-tol workflows are plumbed together by the [included Snakemake
worfklow](./workflow/Snakefile).

## Running the assembly

### Setting up

Clone this repo to the HPC where it will be run.

A profile will be needed to configure the job scheduler on the HPC. Profiles
for [Setonix](./profiles/pawsey) and [Spartan (partial)](./profiles/spartan)
are included. A profile for [local testing](./profiles/local) is also included.

<details>

<summary>More information about the profile</summary>

#### The profile needs at least the following files:

- Snakemake [**job config**](./profiles/pawsey/config.v9+.yaml) and [**workflow
  config**](./profiles/pawsey/workflow.config.yaml): configure the jobs from the
  genome-launcher-workflow.
- [**nextflow config**](./profiles/pawsey/pawsey.config): configure the
  processes from the Sanger-Tol pipelines
- [**ascc.params.config**](./profiles/pawsey/ascc.params.config): the [YAML
  params
  file](https://pipelines.tol.sanger.ac.uk/ascc/0.6.0/usage#running-the-pipeline)
  for ASCC (not shared with the other pipelines).

</details>

### Steps

1. Download the reads and run the QC scripts using the genome-launcher-workflow
   target `pre_genomeassembly`.
2. Run the `genomeassembly` workflow. See the [example 20_genomeassembly.sh
   script](profiles/pawsey/20_genomeassembly.sh).
3. Stage the ASCC reference data using the genome-launcher-workflow target
   `post_genomeassembly`.
4. Run the `ascc` workflow. See the [example 30_ascc.sh
   script](profiles/pawsey/30_ascc.sh).
5. Convert the ASCC output for TreeVal using the genome-launcher-workflow
   target `post_ascc`.
6. If Hi-C is available, run the `treeval` workflow. See the [example
   40_treeval.sh submission script](profiles/pawsey/40_treeval.sh).
7. Run the `post_treeval` target to upload the results to object storage. The
   `post_*` targets all upload the output of the preceding pipeline to object
   storage.
8. **Optional**: curate the genome manually using
   [PretextView](https://github.com/sanger-tol/PretextView). Add the AGP file
   that is output by PretextView and a list of any contigs or scaffolds to
   remove to the repository on GitHub. The files must be named as follows:
   - `curation/{dataset_id}_{assembly_version}_normal_curated_v1.pretext.agp_1`
   - `curation/{dataset_id}.{assembly_version}_scaffolds_to_remove.txt`
9. Once the files from step 8 have been added, pull the updates and run the
   `post_curation` target to split the haplotypes.
10. **Optional**: use the `all_assembly_stats` target to run `seqkit stats
    -all` on the list of expected assembly outputs.
11. **Optional**: use the `upload_all_logs` target to backup all the log files
    to object store.

<details>

<summary>Worked example</summary>

#### Run this assembly on Setonix:

> [!IMPORTANT]
>
> The pull command requires a Personal Access Token with read access to code
> and metadata.

1. Pull the repo:
   1. `git init . `
   2. `git remote add origin https://github.com/AToL-Bioinformatics/xcParTurq1.1.git`
   3. `git pull origin main`
2. Set up the directory structure: `bash profiles/pawsey/00_preflight.sh`
3. Run the workflow steps:
   1. `sbatch profiles/pawsey/10_pre_genomeassembly.sh`
   2. `sbatch profiles/pawsey/20_genomeassembly.sh`
   3. `sbatch profiles/pawsey/25_post_genomeassembly.sh`
   4. `sbatch profiles/pawsey/30_ascc.sh`
   5. `sbatch profiles/pawsey/35_post_ascc.sh`
   6. `sbatch profiles/pawsey/40_treeval.sh`
   7. `sbatch profiles/pawsey/45_post_treeval.sh`
4. Curate manually, add the curation files to the repo, and update the repo:
   1. `git pull origin main`
   2. `sbatch profiles/pawsey/55_post_curation.sh`
5. Generate assembly stats:
   1. `sbatch profiles/pawsey/98_all_assembly_stats.sh`
6. Backup the logs:
   1. `sbatch profiles/pawsey/99_upload_all_logs.sh`

</details>