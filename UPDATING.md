# How to Update the Dataset Repository

This guide explains how to add new datasets to the PreMiEr Dataset Repository website.

## Quick Overview

1. **Add data to spreadsheet** → 2. **Update HTML file** → 3. **Commit & push to GitHub**

## Step-by-Step Instructions

### Step 1: Update the Spreadsheet

1. **Open** `Available_Pending_Datasets.csv` (can use Excel, Google Sheets, or text editor)
2. **Add a new row** with the dataset information
3. **Fill in all required columns** (see [Data Fields](#data-fields) below)
4. **Save as CSV format** (if using Excel: Save As → CSV)

### Step 2: Update the HTML File

1. **Open** `index.html` in a text editor (VS Code, TextEdit, etc.)
2. **Find the datasets array** - search for `const datasets = [`
3. **Add your new dataset** at the end of the array (before the closing `];`)

#### Dataset Format Template

```javascript
{
    projectId:  "YYYY_LastName",
    title:      "Your project title here",
    host:       "Mouse/Human/Environmental",
    sampleType: "Fecal/Wastewater/Plumbing/etc",
    builtEnvironment: "Hospital/Home/Laboratory/Mixed Use/NA",
    sampleSize: "123",
    country:    "US/Bolivia/etc",
    taxa:       "Bacteria/Bacteria and Fungi/Viruses",
    seqTarget:  "16S/WGS/Metagenomics/RNA",
    rawLocation:"NCBI SRA/TBD",
    accession:  "PRJNA1234567/TBD",
    pi:         "Full Name",
    email:      "email@institution.edu",
    institution:"Institution Name",
    status:     "Public/Pending",
    publication:"https://doi.org/... OR In Prep"
},
```

#### Example: Adding a New Dataset

If you have this data:
- Project ID: 2026_Smith
- Title: Gut microbiome in diabetes
- Host: Human
- Sample Type: Fecal
- Sample Size: 75
- PI: John Smith
- Institution: Duke University
- Status: Pending

Add this to the datasets array:

```javascript
{
    projectId:  "2026_Smith",
    title:      "Gut microbiome in diabetes",
    host:       "Human",
    sampleType: "Fecal",
    sampleSize: "75",
    country:    "US",
    taxa:       "Bacteria",
    seqTarget:  "16S",
    rawLocation:"TBD",
    accession:  "TBD",
    pi:         "John Smith",
    email:      "jsmith@duke.edu",
    institution:"Duke University",
    status:     "Pending",
    publication:"In Prep"
},
```

### Step 3: Test Locally (Optional but Recommended)

1. **Open** `index.html` in a web browser
2. **Check** that your new dataset appears in the table
3. **Test** the search and filter functions
4. **Verify** all links work correctly

### Step 4: Commit and Push Changes

1. **Navigate to the repository** in terminal:
   ```bash
   cd "/Users/megan/Desktop/Premier/Data Repository/repository_test"
   ```

2. **Add the changed files**:
   ```bash
   git add "Available_Pending_Datasets.csv" index.html
   ```

3. **Commit the changes**:
   ```bash
   git commit -m "Add new dataset: [Project ID or brief description]

   Co-Authored-By: Claude Sonnet 4 <noreply@anthropic.com>"
   ```

4. **Push to GitHub**:
   ```bash
   git push origin main
   ```

5. **Website updates automatically** - changes appear at https://hillms.github.io/repository_test/ within a few minutes

## Data Fields Reference

### Required Fields

| Field | Description | Notes |
|-------|-------------|-------|
| `projectId` | Format: `YYYY_LastName` | Must be unique |
| `title` | Project title | Keep concise but descriptive |
| `host` | Organism/environment | Mouse, Human, Environmental |
| `sampleType` | Sample material | Can be comma-separated list |
| `builtEnvironment` | Environment type | Hospital, Home, Laboratory, Mixed Use, NA |
| `sampleSize` | Number of samples | Just the number |
| `pi` | Principal investigator | Full name |
| `institution` | PI's institution | Full institution name |
| `status` | Data availability | "Public" or "Pending" |

### Optional Fields

| Field | Description | Default if Empty |
|-------|-------------|------------------|
| `country` | Country of origin | — |
| `taxa` | Microbial type | — |
| `seqTarget` | Sequencing method | — |
| `rawLocation` | Data repository | "TBD" for pending |
| `accession` | BioProject ID | "TBD" for pending |
| `email` | PI contact email | — |
| `publication` | DOI or URL | "In Prep" for unpublished |

### Field Value Guidelines

#### Status
- **"Public"** - Data is available for download
- **"Pending"** - Data will be released later

#### Sample Type
- Can include multiple types: `"Fecal, Lung"`
- Common values: `Fecal`, `Wastewater`, `Plumbing`, `Surface`, `Air`

#### Taxa
- `"Bacteria"`
- `"Bacteria and Fungi"`
- `"Viruses"`

#### Sequencing Target
- `"16S"` - 16S rRNA gene sequencing
- `"WGS"` - Whole genome sequencing
- `"Metagenomics"` - Shotgun metagenomics
- `"RNA"` - RNA sequencing

#### Publication
- Full URLs: `"https://doi.org/10.1234/example"`
- For unpublished: `"In Prep"`

## Common Issues & Solutions

### Problem: Dataset doesn't appear on website
- **Check**: Did you save the HTML file?
- **Check**: Did you add the comma after the previous dataset entry?
- **Check**: Are all quotes matched correctly?

### Problem: Website looks broken
- **Check**: JavaScript syntax - missing commas, quotes, or brackets
- **Test**: Open browser developer tools (F12) and check for errors

### Problem: Filter values don't show up
- **Note**: New filter options auto-populate from existing data
- **Wait**: May take a page refresh to appear in dropdown menus

### Problem: Push to GitHub fails
- **Authentication**: You may need to re-enter your GitHub token
- **Check**: Are you in the correct directory?
- **Retry**: `git push origin main`

## Tips for Success

✅ **Always update both** the spreadsheet AND the HTML file
✅ **Test locally** before pushing to GitHub
✅ **Use consistent formatting** for similar data types
✅ **Double-check spelling** - especially for institution names
✅ **Verify links** work before publishing

## Getting Help

- **Git/GitHub issues**: Ask Megan Hill ([msthoemmes@gmail.com](mailto:msthoemmes@gmail.com))
- **Dataset questions**: Contact the original PI listed in the dataset
- **Website bugs**: Create an issue on GitHub or email Megan

---

**Remember**: Changes to GitHub automatically update the live website within ~5 minutes!