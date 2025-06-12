# Installation Instructions

## Getting Help

If you encounter problems and googling / chatGPTing does not help you can:

- write us on the [slack channel](https://crc1678-inf.slack.com/archives/C090Z8C91M2) or on our email crc1678-inf@uni-koeln.de
- [open an issue](https://github.com/CRC-1678/Teaching-R-basics/issues/new/choose) in this repository
- search on R-specific resources: [R-bloggers](https://www.r-bloggers.com/) and [Posit community](https://forum.posit.co/)
- join on our [pre-course Zoom Q&A]()

## Git

Git is the version control system which is central to modern code development. Git allows you to track and record any changes in your code. [GitHub](https://github.com/) is a popular git hosting and development platform which allows you to share the code with others, collaboratively develop it, test, run and deploy. If you publish your analysis, it will be mandatory for you to provide the code and most likely you will use GitHub for that. Another popular platform, especially in academia, is [GitLab](https://gitlab.com/) - your organization may already provide an institutional account for it.

**Check if you have git installed**
1. Open a terminal.
2. Type the following command and press Enter:
   ```bash
   git --version
   ```
3. If Git is installed, you will see the version number. If not, you will need to install it as described below.

### Install Git

**Windows**

1. Download the Git installer from the [official Git website](https://git-scm.com/download/win).
2. Run the installer and follow the instructions.

**macOS**

1. Open a terminal.
2. Install Homebrew if you haven't already by running:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
3. Install Git using Homebrew:
   ```bash
   brew install git
   ```


**Linux**

1. Open a terminal.
2. Use your package manager to install Git. For example, on Debian/Ubuntu:
   ```bash
   sudo apt update
   sudo apt install git
   ```


### GitHub

If you don't have a GitHub account, create one at https://github.com.

#### Optional: GitHub Desktop

If you prefer a graphical interface for Git, you can use [GitHub Desktop](https://desktop.github.com/).

## R

**Check if you have R installed**
1. Open a terminal.
2. Type the following command and press Enter:
   ```bash
   R --version
   ```
3. If R is installed, you will see the version number. If not, you will need to install it as described below.

### Install R

Install R from the [CRAN website](https://cran.r-project.org/). 

**Windows**

Go to "Download R for Windows" -> "base" -> "Download R x.x.x for Windows" (where x.x.x is the latest version, in our case 4.5.0). Run the installer and follow th instructions.

**macOS**

Go to "Download R for macOS" -> "R-4.x.x.pkg" (where x.x.x is the latest version, in our case 4.5.0). Run the installer and follow the instructions.

**Linux**

Go to "Download R for Linux" and follow the instructions for your specific distribution. For example, for Ubuntu/Debian:
1. Open a terminal.
2. Add the CRAN repository and install R:
   ```bash
   sudo apt update
   # install helper packages
   sudo apt install --no-install-recommends software-properties-common dirmngr
   # add the signing key (by Michael Rutter) for these repos
   # To verify key, run gpg --show-keys /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc 
   # Fingerprint: E298A3A825C0D65DFD57CBB651716619E084DAB9
   wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | sudo tee -a /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc
   # add the repo from CRAN -- lsb_release adjusts to 'noble' or 'jammy' or ... as needed
   sudo add-apt-repository "deb https://cloud.r-project.org/bin/linux/ubuntu $(lsb_release -cs)-cran40/"
   # install R itself
   sudo apt install --no-install-recommends r-base
   ```

### Install Rstudio

RStudio is an integrated development environment (IDE) for R that provides a user-friendly interface and is being maintained by the [Posit](https://posit.co/) company.

Go to the [RStudio download page](https://posit.co/download/rstudio-desktop/) and download the installer for your operating system.

**Windows**

Run the installer (for example, `RStudio-2025.05.1-513.exe`) and follow the instructions.

**macOS**

Run the installer (for example, `RStudio-2025.05.1-513.dmg`) and follow the instructions.

**Linux**
1. Open a terminal.
2. Download the latest RStudio .deb package, for example `rstudio-2025.05.1-513-amd64.deb`.
3. Install the package using the following command:
   ```bash
   sudo dpkg -i rstudio-*.deb
   ```

Launch RStudio after installation and follow the instructions to create an R project and install necessary packages.

Packages we will need: "knitr", "rmarkdown"

### Install R packages
To install R packages, you can use the following command in the R console:
```R
install.packages()
```

### Upgrading

You will need to upgrade R and RStudio on a regular basis to be able to use newer packages and get latest developments and fixes.

**R**

**RStudio**

**R packages**


### Uninstalling

This project sets up a learning environment locally, but you may decide to switch to a different setup, be it conda or a containerized environment or the RStudio server provided on your HPC cluster. In this case, you may want to uninstall the software you installed on your local laptop.

**R**

**RStudio**

**R packages**

To uninstall a single package, type the R console:
```R
remove.packages("package_name")
```

