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
cd /home
pwd
```

4. Check if you have **wget** and install if necessary

[Mac instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Mac)

[Windows instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Windows)

5. Try downloading an external file
```bash
wget https://adimitromanolakis.github.io/truffle/fs-and-po-pairs-from-1000genomes.vcf.gz
```


**EXERCISE**: What is the file size of downloaded file HG001_chr22.vcf.gz?
Find it out from the docker terminal by running ```ls -hl```


6. Unzip the .gz file (depends on Operating System)
```bash
gunzip fs-and-po-pairs-from-1000genomes.vcf.gz
```

7. Print the last ten lines of the .vcf file
```bash
tail -n 10 fs-and-po-pairs-from-1000genomes.vcf
```

**EXERCISE**: What is the the number of lines in .vcf file fs-and-po-pairs-from-1000genomes.vcf?
Find it out from the docker terminal by running ```wc -l fs-and-po-pairs-from-1000genomes.vcf```


**EXERCISE**: What is the the md5 value of the last ten lines of the file fs-and-po-pairs-from-1000genomes.vcf?
Find it out from the docker terminal by running ```tail -n 10 fs-and-po-pairs-from-1000genomes.vcf | md5sum ```

8. Search the line containing the SNP with RSID rs2401506.
```bash
grep rs2401506 fs-and-po-pairs-from-1000genomes.vcf
```


9. Create your own directory
```bash
mkdir variants
ls -hl
```

10. Copy a file
```bash
cp fs-and-po-pairs-from-1000genomes.vcf testcopy.vcf
ls -hl
```

11. Move a file to another directory
```bash
mv testcopy.vcf variants
ls -hl
ls -hl variants
```

