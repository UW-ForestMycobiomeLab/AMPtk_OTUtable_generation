# AMPtk_OTUtable_generation

## This code is written assuming the following file structure; download your zipped files into a Project folder (descriptive name) and call that downloaded file “raw_data/sequencing” and don't forget to duplicate this into a private Zenodo repo!

```         
project_root/
│
├── raw_data/  # Renamed for consistency (lowercase and underscores)
│   └── sequencing/  # Directory containing raw sequencing reads
│       └── (your raw zipped sequence files here, e.g., *.fastq.gz)
│
├── results/  # Renamed for simplicity (instead of amptk_results/)
│   ├── amptk/  # Subdirectory for AMPtk-specific outputs
│   │   ├── ITS_OTU_table.biom  # OTU table in BIOM format
│   │   ├── ProcessedReads.demux.fq.gz  # Demultiplexed sequencing reads
│   │   ├── ProcessedReads.cluster.otus.fa  # Clustered OTUs
│   │   ├── ProcessedReadsClean.cluster.otus.fa  # Filtered OTU clusters
│   │   └── ProcessedReadsClean.otu_table.txt  # OTU table after filtering
│   └── phyloseq/  # Subdirectory for phyloseq-related outputs
│       └── FungiPhyloseqData.rds  # Saved phyloseq object for downstream analysis
│
├── data/  # Directory for metadata and other input files
│   ├── metadata/  # Subdirectory for metadata files
│   │   ├── SequencingID.txt  # Sequencing sample key
│   │   ├── Metadata.csv  # Environmental data with sample names matching SequencingID.txt
│   │   └── README.md  # Metadata documentation (e.g., column descriptions, units)
│   └── references/  # Optional: Subdirectory for reference files (e.g., databases, taxonomies)
│
├── scripts/  # Directory for analysis scripts
│   ├── 1_amptk_fungal_pipeline.Rmd  # AMPtk processing scripts 
│   └──2_quick_analysis.Rmd  # Quick plotting in R
│
├── AMPtk_OTU_Table_Generation.Rproj  # R Project file for OTU table generation (renamed for consistency)
│
└── README.md  # Project overview and setup instructions (e.g., AMPtk settings, dependencies)
```
