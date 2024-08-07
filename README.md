
# Overview

- 1. Python scripts: convert_eprime_to_bids_event.py, qc_eventsfiles.py
- 2. Two json files describing the headers of the convert_eprime_to output files.

# Scripts
## convert eprime to bids event

You should have one zipped directory per participant, each containing the following 3 .txt files generated by eprime at the time of testing:
- Onset-Event-Encoding_CIMAQ_*.txt
- Output_Retrieval_CIMAQ_*.txt
- Output-Responses-Encoding_CIMAQ*.txt

It Two .tsv files per participant

- `sub-**-ses-*_task-memory_events.tsv` (** = dccid, * = session ID)

This file is used to create event files in Nistats/Nilearn (to label fMRI frames)
Note: the TaskFile_headers_CIMAQ_memory.json file describes the metrics found in each column.

- `sub-**-ses-*_post-scan-behav.tsv` (** = dccid, * = session ID)

This file is to assess a participant's performance on the post-scan
memory task (image and source recognition).
Note: the PostScanBehav_CIMAQ_memory.json file describes the metrics saved in each column

For more information please use --help.

## QC event files

It uses the tsv files and save a QC report.

For more information please use --help.

# Thank you

Code originaly provided by @MarieStLaurent
Later modified by @PierreEMorin
