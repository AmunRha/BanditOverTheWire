# BanditOverTheWire

Short Write-Up for Bandit Wargames from <a href = "https://overthewire.org/wargames/bandit/bandit1.html">overthewire.org</a> till Level 15


## bandit0 -> bandit1

[*] Used ssh cmd to login 

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
bandit0 - boJ9jbbUNNfktd78OOpsqOltutMc3MY1

## bandit1 -> bandit2

[*] Used cat cmd to read file

```bash
cat readme
```
bandit1 - CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

## bandit2 -> bandit3

[*] Used cat cmd to read file with special char

```bash
cat ./-
```
bandit2 - UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

## bandit3 -> bandit4

[*] Used cmd command to read file with spaces

```bash
cat "spaces in this filename"
```
bandit3 - pIwrPrtPN36QITSp3EQaw936yaFoFgAB

## bandit4 -> bandit5

[*] Used cd to navigate into ./inhere dir

```bash
cd inhere
```
[*] And cat to read file

```bash
cat [filename]
```
bandit4 - koReBOKuIDDepwhWk7jZC0RTdopnAYKh

## bandit5 -> bandit6

[*] Used cd to navigate into ./inhere dir

```bash
cd inhere
```
[*] Used find cmd to find file with 1033 bytes 

```bash
find * -size 1033c
```
[*] Used cat cmd to read file

```bash
cat maybehere07/.file2
```
bandit5 - DXjZPULLxYr17uwoI01bNLQbtFemEgo7

## bandit6 -> bandit7

[*] Used cd to navigate to the top of tree(root folder)

[*] Used find with size,user,group options and removed all err 
    statements using 2>/dev/null

```bash
find -size 33c -user bandit7 -group bandit6 2>/dev/null
```
bandit6 - HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

## bandit7 -> bandit8

[*] Used cat to read file and piped to grep to find the passwd

```bash
cat data.txt | grep millionth
```
bandit7 - cvX2JJa4CFALtqS87jk27qwqGhBM9plV

## bandit8 -> bandit9

[*] Used cat to read file 

```bash
cat data.txt
```
[*] Piped it to sort without any options

```bash
cat data.txt | sort
```
[*] Piped that to uniq with option -u to report unique lines

```bash
cat data.txt | sort | uniq -u
```
bandit8 - UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

## bandit9 -> bandit10

[*] Used strings to print out human readable texts

```bash
strings data.txt
```
[*] Piped it to grep to print out texts with multiple "==="

```bash
strings data.txt | grep ===
```
bandit9 - truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

## bandit10 -> bandit11

[*] Used cat to read the file

```bash
cat data.txt
```
[*] Piped it to base64 with option -d to decode data

```bash
cat data.txt | base64 -d
```
bandit10 - IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

## bandit11 -> bandit12

[*] Used cat to read the file

```bash
cat data.txt
```
[*] Used tr to replace all characters in set A-Z and a-z with 
    all corresponding characters in set N-Z,A-M and n-z,a-m

```bash
cat data.txt | tr "A-Za-z" "N-ZA-Mn-za-m"
```
bandit11 - 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

## bandit12 -> bandit13

[*] Used xxd with option -r to convert hexdump to data file

```bash
xxd -r data.txt > file
```
[*] Used file option to find the archive type and renamed the 
    original file with the respective archive extension and 
    respectively used tar,gzip,bzip2 to decompress the file

```bash
file [filename]

mv [filename1] [filename2].[archiveType]

tar -xf [filename].tar

gzip -d [filename].gz 

bzip2 -d [filename].bz
```
bandit12 - 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

## bandit13 -> bandit14

[*] Retrieved ssh private keys and saved it under .ssh/id_rsa

[*] Changed the file permission to 600

```bash
chmod 600 id_rsa
```
[*] Singed in using the private key for user bandit14

```bash
ssh -i id_rsa bandit14@bandit.labs.overthewire.org -p 2220
```
[*] Navigated to /etc/bandit_pass and used cat to read the password

bandit14 - 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

## bandit14 -> bandit15

[*] Used nc to connect to port 30000 using host as "localhost"

```bash
nc localhost 30000
```
bandit15 - BfMYroe26WYalil77FoDi9qh59eK5xNr

## bandit15 -> bandit16

[*] Used openssl to connect to "localhost" at port 30001

```bash
openssl s_client -connect localhost:30001
```
bandit16 - cluFn7wTiGryunymYOu4RcffSxQluehd
