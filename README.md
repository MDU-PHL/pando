
# pando
With an excel spreadsheet LIMS request, run QC analyses on isolates

### Example run command on MDU servers:
`pando run LIMS_DATA_20160801.xlsx`


### Get help:
```
pando -h
usage: pando [-h] [-w WGS_QC] [-N] [-k] [-t THREADS] [-a] [-r] [-m]
             [-s MODEL_ANDI_DISTANCE] [-c PERCENT_CUTOFF] [-v]
             mdu_read_IDs

Run QC summary analysis.

positional arguments:
  mdu_read_IDs          Excel spreadsheet LIMS request.

optional arguments:
  -h, --help            show this help message and exit
  -w WGS_QC, --wgs_qc WGS_QC
                        Path to WGS QC (default: /mnt/seq/MDU/QC/)
  -N, --Nullarbor_folders
                        Are you running this on a set of folders generated by
                        Nullarbor? (default: False)
  -k, --keep_tempdirs   Keep tempdirs created during run? (default: False)
  -t THREADS, --threads THREADS
                        Number of threads (default: 72)
  -a, --andi_run        Run andi phylogenomic analysis? (default: False)
  -r, --roary_run       Run roary pangenome analysis? (default: False)
  -m, --metadata_run    Gather metadata for all isolates? (default: True)
  -s MODEL_ANDI_DISTANCE, --model_andi_distance MODEL_ANDI_DISTANCE
                        Substitution model. 'Raw', 'JC', or 'Kimura'.
                        (default: JC)
  -c PERCENT_CUTOFF, --percent_cutoff PERCENT_CUTOFF
                        For abricate, call the gene 'present' if greater than
                        this value and 'maybe' if less than this value.
                        (default: 95)
  -v, --version         Print version number and exit. (default: False)
```

