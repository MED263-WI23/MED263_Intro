## Basic linux commands

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

4. Try downloading an external file
```bash
wget https://github.com/jihoonkim/dockerhub-iadmix/raw/master/HG001_chr22.vcf.gz
```

5. Install missing package **wget** first and try again downloading the file
[Mac instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Mac)
[Windows instructions](https://www.jcchouinard.com/wget/#Download_Wget_on_Windows)

**EXERCISE**: What is the file size of downloaded file HG001_chr22.vcf.gz?
Find it out from the docker terminal by running ```ls -hl```

6. Unzip the .gz file (depends on Operating System)
```bash
gunzip HG001_chr22.vcf.gz
```

7. Print the last ten lines of the .vcf file
```bash
tail -n 10 HG001_chr22.vcf
```

**EXERCISE**: What is the the number of lines in .vcf file HG001_chr22.vcf?
Find it out from the docker terminal by running ```wc -l HG001_chr22.vcf```


**EXERCISE**: What is the the md5 value of the last ten lines of the file HG001_chr22.vcf?
Find it out from the docker terminal by running ```tail -n 10 HG001_chr22.vcf | md5sum ```

8. Search the line containing the SNP with RSID rs2401506.
```bash
grep rs2401506 HG001_chr22.vcf
```


9. Create your own directory
```bash
mkdir variants
ls -hl
```

10. Copy a file
```bash
cp HG001_chr22.vcf testcopy.vcf
ls -hl
```

11. Move a file to another directory
```bash
mv testcopy.vcf variants
ls -hl
ls -hl variants
```


**EXERCISE**: What are the reference allels and alternative alleles of SNP rs2401506 in this .vcf file? Find it out from the docker terminal by running ```tail -n 10 HG001_chr22.vcf | md5sum ```


**EXERCISE**: Read and follow the [Interactive VIM tutorial](http://www.openvim.com/tutorial.html).  We will cover the earlier part during the class, but be sure to finish the rest at home by next class.
