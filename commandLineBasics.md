## Basic linux commands
1. Update the Ubuntu packages
```bash
# inside the docker instance
apt-get update
```

2. Display the current directory
```bash
# inside the docker instance
pwd
```

3. Change to a different directory and check if the current directory has been changed
```bash
# inside the docker instance
cd /home
pwd
```

4. Try downloading an external file
```bash
# inside the docker instance
wget https://github.com/jihoonkim/dockerhub-iadmix/raw/master/HG001_chr22.vcf.gz
```

5. Install missing package **wget** first and try again downloading the file
```bash
# inside the docker instance
apt-get install wget
wget https://github.com/jihoonkim/dockerhub-iadmix/raw/master/HG001_chr22.vcf.gz
```
**EXERCISE 6**: What is the file size of downloaded file HG001_chr22.vcf.gz?
Find it out from the docker terminal by running ```ls -hl```

6. Try extracting the compressed file in .gz format while keeping the original file
```bash
# inside the docker instance
gunzip -k HG001_chr22.vcf.gz
```

7. Install missing package **zip** first and try again extracting the file
```bash
# inside the docker instance
apt-get install zip
gunzip -k HG001_chr22.vcf.gz
ls -hl
```

8. Print the last ten lines of the .vcf file
```bash
# inside the docker instance
tail -n 10 HG001_chr22.vcf
```

**EXERCISE 7**: What is the the number of lines in .vcf file HG001_chr22.vcf?
Find it out from the docker terminal by running ```wc -l HG001_chr22.vcf```


**EXERCISE 8**: What is the the md5 value of the last ten lines of the file HG001_chr22.vcf?
Find it out from the docker terminal by running ```tail -n 10 HG001_chr22.vcf | md5sum ```

9. Search the line containing the SNP with RSID rs2401506.
```bash
# inside the docker instance
grep rs2401506 HG001_chr22.vcf
```


10. Create your own directory
```bash
# inside the docker instance
mkdir variants
ls -hl
```

11. Copy a file
```bash
# inside the docker instance
cp HG001_chr22.vcf testcopy.vcf
ls -hl
```

12. Move a file to another directory
```bash
# inside the docker instance
mv testcopy.vcf variants
ls -hl
ls -hl variants
```

13. Install VIM editor and start using it
```bash
# inside the docker instance
apt-get install vim
vim myfile.txt
```

**EXERCISE 9**: What are the reference allels and alternative alleles of SNP rs2401506 in this .vcf file? Find it out from the docker terminal by running ```tail -n 10 HG001_chr22.vcf | md5sum ```


**EXERCISE 10**: Read and follow the [Interactive VIM tutorial](http://www.openvim.com/tutorial.html).  We will cover the earlier part during the class, but be sure to finish the rest at home by next class.
