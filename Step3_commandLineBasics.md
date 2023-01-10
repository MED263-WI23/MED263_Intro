## Basic commands

1. List the contents of the current directory
```bash
ls
```

2. Display the current directory path
```bash
pwd
```

3. Create your own directory
```bash
mkdir ~/variants
```

4. Change to a different directory and check if the current directory has been changed
```bash
cd ~/variants
pwd
```

5. Check if you have **wget** and install if necessary

Mac
```bash
# Check if wget is installed
wget --version

# If wget is not installed, check if homebrew is installed
brew --version

# If brew is not installed, install it:
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install wget using brew
brew install wget

# Confirm that it worked
wget --version
```
[Mac instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Mac)

Linux/Ubuntu
```bash
# See if wget is installed
wget --version

# Install 
apt-get install wget

# Confirm that it worked
wget --version
```
[Linux instructions](https://www.tecmint.com/install-wget-in-linux/)

Windows users: Follow Ubuntu instructions above if you have installed Ubuntu.
If not, instructions are here:
[Windows instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Windows)

6. Try downloading an external file
```bash
wget https://adimitromanolakis.github.io/truffle/fs-and-po-pairs-from-1000genomes.vcf.gz
```

7. Find the file size of fs-and-po-pairs-from-1000genomes.vcf by running 
```bash
ls -hl
```

8. Unzip the .gz file (depends on Operating System)
Mac
```bash
# Check if gzip is installed
gzip --version

# If not, install it using brew
brew install gzip

# Unzip the .gz file
gunzip fs-and-po-pairs-from-1000genomes.vcf.gz
```

Ubunutu
```bash
# Check if gzip is installed
gzip --version

# If not, install it
sudo apt install gzip

# Unzip the .gz file
gunzip fs-and-po-pairs-from-1000genomes.vcf.gz
```

9. Print the last ten lines of the .vcf file
```bash
tail -n 10 fs-and-po-pairs-from-1000genomes.vcf
```

10. Find the number of lines in .vcf file fs-and-po-pairs-from-1000genomes.vcf
```bash
wc -l fs-and-po-pairs-from-1000genomes.vcf
```

11. Copy a file
```bash
cp fs-and-po-pairs-from-1000genomes.vcf testcopy.vcf
ls -hl
```


12. Move a file to another directory
```bash
mkdir newDir
mv testcopy.vcf newDir
ls -hl
ls -hl newDir
```
