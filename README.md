# Fine Merger Studio (v3.1) — by Alkyr

A standalone Windows tool for merging, converting, and extracting genetic datasets (**AADR / Reich Lab / 1240K / HO**) and personal raw DNA files for **qpAdm / AdmixTools** modeling.

- **Single `.exe` file** — No WSL, Linux, Python, or PLINK installation required.
- **Zero External Dependencies** — Native 64-bit Windows EIGENSOFT (`convertf`, `mergeit`) and `PLINK` are built right inside the app.

---

## ⚠️ Important Before Starting: Raw DNA Format
If you are using your own personal DNA file, **it must be in 23andMe raw data format** (`.txt`).

- If your DNA file is from **AncestryDNA, MyHeritage, FTDNA, LivingDNA**, etc., first convert it to **23andMe format** using the free **[DNAGenics DNA Kit Studio](https://www.dnagenics.com/dna-kit-studio/)** (*Raw Data Converter -> Convert to 23andMe*).

---

## ⚡ Quick Start: How to Merge Your Raw DNA with AADR in 1 Click
*(For beginners who just want to model themselves in qpAdm / AdmixTools)*

Open the app and go to **Tab 03: `⚡ Raw to PLINK & Auto-Merge`**:

1. **23andMe Raw File:** Click **Browse Raw...** and select your 23andMe format DNA file.
2. **Sample Name & Sex *(Optional)*:** Type your name/alias (e.g. `MySample`) and choose your sex (`Male` or `Female`). This is the name you will see inside the `.ind` file.
3. **AADR Reference Dataset:** In the lower box, click **Browse AADR File...** and select any file (`.geno`, `.snp`, or `.ind`) from your downloaded AADR / HO / 1240K dataset.
4. **Target Output Folder:** Choose where you want your final merged files to be saved.
5. **Click the Green Button:**
   > **`⚡ FULL PIPELINE: Raw → PACKEDANCESTRYMAP → Merge with AADR`**

**Done!** The app will automatically:
1. Clean and sort your raw DNA with PLINK,
2. Convert it to `PACKEDANCESTRYMAP` format,
3. Merge it with the AADR dataset,
4. Delete all temporary files and leave you with your ready-to-use `.geno`, `.snp`, and `.ind` files.

---

## Other Tabs Guide

### `01 ⊕ Merge Datasets`
Use this tab when you already have two datasets (e.g., `.geno / .snp / .ind`) and want to combine them into one dataset.
1. Select **Dataset 1** (Main/Reference dataset).
2. Select **Dataset 2** (Second dataset).
3. Choose an output location and click **`⊕ MERGE DATASETS NOW`**.

### `02 ⇄ Convert Format`
Use this tab to convert a dataset between different genetic formats:
- **PLINK Binary (`PACKEDPED`):** `.bed / .bim / .fam`
- **PLINK Text (`PED`):** `.ped / .map`
- **AdmixTools Binary (`PACKEDANCESTRYMAP`):** `.geno / .snp / .ind` *(packed, small file size)*
- **AdmixTools Text (`EIGENSTRAT`):** `.geno / .snp / .ind` *(uncompressed text)*

Select your source file, pick your target format, and click **`⇄ CONVERT FORMAT NOW`**.

### `04 ✂ Extract Populations`
Use this tab to create a smaller dataset containing only specific populations from a huge dataset (like AADR):
1. Select your source dataset file (`.geno`, `.snp`, or `.ind`).
2. Click **`📋 Load Populations from Dataset .ind`** to search and select populations from the list *(or type/paste population names separated by commas)*.
3. Choose an output file name and click **`✂ EXTRACT POPULATIONS NOW`**.
