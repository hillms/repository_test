# PreMiEr Dataset Repository

A web-based catalog of microbiome datasets from PreMiEr (Precision Microbiome Engineering) research projects.

**🌐 Live Website**: https://hillms.github.io/repository_test/

## Overview

This repository contains an interactive webpage that displays available and pending microbiome datasets from PreMiEr research collaborations. Researchers can search and filter datasets by various criteria including host organism, sample type, microbial taxa, institution, and publication status.

## Files in This Repository

| File | Purpose |
|------|---------|
| `index.html` | Main webpage - displays the dataset repository |
| `Available and Pending Datasets.xlsx` | Source data spreadsheet |
| `README.md` | This documentation file |
| `UPDATING.md` | Step-by-step guide for adding new datasets |

## Features

- **Interactive Search**: Free-text search across all dataset fields
- **Advanced Filtering**: Filter by host, sample type, microbial taxa, institution, status
- **Direct Data Access**: Links to NCBI SRA for downloading raw sequencing data
- **Publication Links**: Direct links to associated research publications
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Real-time Statistics**: Displays counts of total, public, and pending datasets

## Current Dataset Statistics

- **Total Datasets**: 10
- **Public**: 6 (available for download)
- **Pending**: 4 (awaiting publication/release)
- **Institutions**: Duke University, UNC Charlotte, NC A&T, UNC Chapel Hill

## Dataset Categories

### Host Organisms
- Mouse
- Human
- Environmental samples

### Sample Types
- Fecal samples
- Wastewater
- Plumbing systems
- Lung tissue
- Air samples
- Surface swabs

### Sequencing Methods
- 16S rRNA gene sequencing
- Whole genome sequencing (WGS)
- Metagenomics
- RNA sequencing

## How to Add New Datasets

See [`UPDATING.md`](UPDATING.md) for detailed instructions on adding new datasets to the repository.

## Data Fields

Each dataset includes the following information:

| Field | Description | Example |
|-------|-------------|---------|
| Project ID | Unique identifier | `2026_Hill` |
| Project Title | Descriptive title | `Temporal stability of bacterial communities...` |
| Host | Organism or environment | `Environmental` |
| Sample Type | Type of sample collected | `Plumbing` |
| Sample Size | Number of samples | `144` |
| Country | Country where samples collected | `US` |
| Microbial Taxa | Type of microorganisms | `Bacteria` |
| Sequencing Target | Sequencing method | `16S` |
| Raw Data Location | Repository | `NCBI SRA` |
| Accession Number | BioProject accession | `PRJNA1363208` |
| PI | Principal investigator | `Claudia K. Gunsch` |
| Email | PI contact email | `ckgunsch@duke.edu` |
| Institution | Affiliated institution | `Duke University` |
| Status | Availability status | `Public` or `Pending` |
| Publication | DOI or URL | Link to publication |

## Technical Details

- **Framework**: Pure HTML/CSS/JavaScript (no dependencies)
- **Hosting**: GitHub Pages
- **Data Format**: JavaScript array embedded in HTML
- **Styling**: Custom CSS with PreMiEr branding colors
- **Responsive**: Mobile-friendly design

## Contributing

To contribute new datasets or suggest improvements:

1. Update the spreadsheet (`Available and Pending Datasets.xlsx`)
2. Follow the updating instructions in [`UPDATING.md`](UPDATING.md)
3. Test the changes locally
4. Commit and push to GitHub

## Contact

For questions about specific datasets, contact the listed Principal Investigator directly.

For technical issues with this repository, contact [Megan Hill](mailto:msthoemmes@gmail.com).

---

**Last Updated**: March 2026
**Maintained by**: PreMiEr Research Collaboration
**Data Source**: NCBI SRA and collaborating institutions