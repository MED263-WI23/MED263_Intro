## Basic commands

1. List the contents of the current directory
```bash
ls
```

2. Display the current directory path
```bash
pwd
```

3. Change to a different directory and check if the current directory has been changed
```bash
cd ~
pwd
```

4. Check if you have **wget** and install if necessary

[Mac instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Mac)

[Windows instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Windows)

5. Try downloading an external file
```bash
wget https://adimitromanolakis.github.io/truffle/fs-and-po-pairs-from-1000genomes.vcf.gz
```

6. Find the file size of fs-and-po-pairs-from-1000genomes.vcf by running 
```bash
ls -hl
```

7. Unzip the .gz file (depends on Operating System)
```bash
gunzip fs-and-po-pairs-from-1000genomes.vcf.gz
```

8. Print the last ten lines of the .vcf file
```bash
tail -n 10 fs-and-po-pairs-from-1000genomes.vcf
```

9. Find the number of lines in .vcf file fs-and-po-pairs-from-1000genomes.vcf
```bash
wc -l fs-and-po-pairs-from-1000genomes.vcf
```

10. Create your own directory
```bash
mkdir variants
ls -hl
```

11. Copy a file
```bash
cp fs-and-po-pairs-from-1000genomes.vcf testcopy.vcf
ls -hl
```

12. Move a file to another directory
```bash
mv testcopy.vcf variants
ls -hl
ls -hl variants
```
