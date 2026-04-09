# Data Access

This repository uses **Git Large File Storage (Git LFS)** to manage large files. The dataset is not stored directly in standard Git history; instead, Git LFS stores a lightweight pointer file in the repository and downloads the actual dataset separately.

To access the dataset, please follow the steps below.

***

### 1. Install Git LFS

Before cloning or pulling the repository, ensure that Git LFS is installed on your system.

#### macOS (Homebrew)

```bash
brew install git-lfs
```

#### Ubuntu / Debian

```bash
sudo apt install git-lfs
```

#### Windows

Download and install Git LFS from:
<https://git-lfs.github.com/>

After installation, initialize Git LFS:

```bash
git lfs install
```

***

### 2. Clone the Repository

Once Git LFS is installed, clone the repository as usual:

```bash
git clone https://github.com/carsonordyna/STAT-486-Final-Project.git
```

Then navigate into the project directory:

```bash
cd STAT-486-Final-Project
```

Git LFS will automatically download the large dataset file during the clone process.

***

### 3. Pulling the Dataset (If Already Cloned)

If you cloned the repository **before** installing Git LFS, the dataset file may appear as a small text pointer instead of the actual data.

To download the dataset:

```bash
git lfs pull
```

***

### 4. Dataset Location

After a successful clone or pull, the dataset can be found at:

    data/lung_cancer_data.csv

The associated data documentation is available at:

    data/data_dictionary.pdf

***

### 5. Verifying Git LFS Is Working (Optional)

To confirm that the dataset is tracked using Git LFS, run:

```bash
git lfs ls-files
```

You should see the dataset file listed.

***

### Notes

*   Git LFS is required to access the full dataset.
*   Without Git LFS, only a placeholder file will be downloaded.
