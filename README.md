# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

![Screenshot 2025-05-11 211224](https://github.com/user-attachments/assets/3353c3e3-ef18-4672-ba45-3af1f0dfb9a1)


cat < file2
## OUTPUT
![Screenshot 2025-05-11 211305](https://github.com/user-attachments/assets/3f618715-8196-4c9d-a28f-89ff53ecb481)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot 2025-05-11 211333](https://github.com/user-attachments/assets/b0376cac-4095-436d-90d9-75c0e2229e0e)

comm file1 file2
 ## OUTPUT
![Screenshot 2025-05-11 211424](https://github.com/user-attachments/assets/27392e17-0444-4887-8cf4-2b1a98372680)

 
diff file1 file2
## OUTPUT

![Screenshot 2025-05-11 211450](https://github.com/user-attachments/assets/fc14e31d-3e48-4e9a-8154-eeb544dd73d1)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![Screenshot 2025-05-11 211531](https://github.com/user-attachments/assets/d0576d2b-a4d8-47ba-805a-bbbf282ab6ac)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2025-05-11 211601](https://github.com/user-attachments/assets/89222806-6ac5-429f-8516-71f2432f2a4b)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-05-11 211633](https://github.com/user-attachments/assets/5b87a8de-6dbb-488e-8338-037c2c0972db)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![Screenshot 2025-05-11 211701](https://github.com/user-attachments/assets/6098549b-b8bd-4077-9ba1-afc5b6767d4d)


grep hello newfile 
## OUTPUT

![Screenshot 2025-05-11 211733](https://github.com/user-attachments/assets/39cc46a4-3661-40e4-863b-66e94f0155a1)



grep -v hello newfile 
## OUTPUT

![Screenshot 2025-05-11 211812](https://github.com/user-attachments/assets/81e93202-870a-4656-a8d1-9552ae64a3ad)


cat newfile | grep -i "hello"
## OUTPUT


![Screenshot 2025-05-11 211841](https://github.com/user-attachments/assets/d788ee3f-5ffd-4847-b732-623e87bd3a39)


cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2025-05-11 212019](https://github.com/user-attachments/assets/9ba36031-70d9-45c2-853e-267c86ffcee4)



grep -R ubuntu /etc
## OUTPUT

![Screenshot 2025-05-11 212045](https://github.com/user-attachments/assets/c180d7de-9a4d-4f25-95ab-ae3ca7e236c6)


grep -w -n world newfile   
## OUTPUT

![Screenshot 2025-05-11 212118](https://github.com/user-attachments/assets/50e2dff9-ef66-4c17-9464-44a24aa35e35)

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![Screenshot 2025-05-11 212143](https://github.com/user-attachments/assets/b02a4cc8-5ba9-45f8-8cb1-cf01dd439b64)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2025-05-11 212213](https://github.com/user-attachments/assets/f656b940-cb2b-426b-9dce-2c6f0d9f6d2c)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2025-05-11 212242](https://github.com/user-attachments/assets/646161b7-7a49-4a42-b338-7e817580fe28)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2025-05-11 212308](https://github.com/user-attachments/assets/98e18890-8526-4aef-965c-c1809d5b3344)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-05-11 212336](https://github.com/user-attachments/assets/be3b65bd-94a5-46d6-adf3-1378cb7ab04e)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot 2025-05-11 212403](https://github.com/user-attachments/assets/0c78328d-a924-4495-ba3b-76bfb7fa7c23)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2025-05-11 212430](https://github.com/user-attachments/assets/649c97eb-b5e1-4acf-8eab-a1e72be7551d)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2025-05-11 212453](https://github.com/user-attachments/assets/340ba8c9-83ba-439a-a5bd-8789cfd6fa82)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2025-05-11 212518](https://github.com/user-attachments/assets/16f0cb32-e506-4872-b48a-71c730c16a67)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2025-05-11 212544](https://github.com/user-attachments/assets/35c49927-b60d-485f-96ca-922b67616029)

egrep l{2} newfile
## OUTPUT
![Screenshot 2025-05-11 212612](https://github.com/user-attachments/assets/2b2f5e1d-efe6-4b22-aaea-046ff8e55b52)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-05-11 212657](https://github.com/user-attachments/assets/c6420885-8339-4785-a5b6-43f0cf6f5853)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

![Screenshot 2025-05-11 212934](https://github.com/user-attachments/assets/8368d1a3-2d28-40a4-b81d-ba1c91f491fd)


sed -n -e '$p' file23
## OUTPUT

![Screenshot 2025-05-11 213001](https://github.com/user-attachments/assets/515f12a4-f11c-4ba2-8148-4b006fe3e5de)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-05-11 213027](https://github.com/user-attachments/assets/7cb09d75-c89a-4a51-8f94-31dc31bde3e4)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-11 213053](https://github.com/user-attachments/assets/a015d00e-d3df-4dba-ae32-b8d474c8eaa5)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2025-05-11 213212](https://github.com/user-attachments/assets/a674fd4d-d4a8-4302-90db-e0fe08b85232)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-05-11 213237](https://github.com/user-attachments/assets/fe6c283f-d4a6-40c2-a0da-42c4b67e83e4)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot 2025-05-11 213309](https://github.com/user-attachments/assets/023a2db7-4085-41bd-b666-998263f75b5b)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-11 213331](https://github.com/user-attachments/assets/e19f6f27-d064-4fd2-a265-685908f5b2cd)



seq 10 
## OUTPUT

![Screenshot 2025-05-11 213427](https://github.com/user-attachments/assets/73af8b9e-7ab6-4a8c-ac8f-5a85f1627744)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2025-05-11 213451](https://github.com/user-attachments/assets/0113fa9e-9d2a-43c6-95f8-7fea6b24ada6)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2025-05-11 213605](https://github.com/user-attachments/assets/61ef70bb-430e-40d0-a02b-fcf26e15eb7b)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2025-05-11 213641](https://github.com/user-attachments/assets/7c0f24c7-e8e8-45e0-ad0b-7518bad2c57b)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2025-05-11 213950](https://github.com/user-attachments/assets/24ec3804-9386-40e0-bb91-40b72a5161f7)

seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2025-05-11 214405](https://github.com/user-attachments/assets/0d9295a5-72ca-4fae-bcc6-d67b1f062f57)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot 2025-05-11 214434](https://github.com/user-attachments/assets/1ff6a2c5-0307-474f-9c5a-3495f0ebd849)



sed -n '2,4{s/$/*/;p}' file23
![Screenshot 2025-05-11 214518](https://github.com/user-attachments/assets/266fc010-e38a-4f3b-82a1-1202a0b9e762)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

![Screenshot 2025-05-11 214552](https://github.com/user-attachments/assets/d4dccf55-4a14-47ec-876e-4f2a2dcb441e)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![Screenshot 2025-05-11 214635](https://github.com/user-attachments/assets/b00674ea-4bbb-4c58-8907-07358534d52b)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-05-11 214713](https://github.com/user-attachments/assets/91aa10ad-7adc-4413-b3a8-8801e2716e57)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

![Screenshot 2025-05-11 214740](https://github.com/user-attachments/assets/0c4299bb-4b05-4a4b-8111-54ffdb179e80)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-05-11 214805](https://github.com/user-attachments/assets/18865692-40f3-4cc3-8b9d-12eb8d1649ec)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2025-05-11 214832](https://github.com/user-attachments/assets/23663956-a214-421e-a1f5-b5c1a1b3448a)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![Screenshot 2025-05-11 215033](https://github.com/user-attachments/assets/d4116d67-b9b0-44ff-b186-abeddf83a7e3)

tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-05-11 215059](https://github.com/user-attachments/assets/d4dfe0f4-135e-4e2e-b3bb-8e34722f27a0)

gzip backup.tar

ls .gz
## OUTPUT
 ![Screenshot 2025-05-11 215123](https://github.com/user-attachments/assets/c4c56e28-7003-4fe3-b909-ae35461c2606)

gunzip backup.tar.gz
## OUTPUT
![Screenshot 2025-05-11 215146](https://github.com/user-attachments/assets/2fb0cc79-e02b-432c-a9e5-d2e88a5c5354)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot 2025-05-11 220024](https://github.com/user-attachments/assets/dbd66057-3e3b-4eff-9794-98bee19f7dbd)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2025-05-11 220120](https://github.com/user-attachments/assets/ecbfe38b-0a84-4e99-9486-abe0cbd57db1)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![Screenshot 2025-05-11 220148](https://github.com/user-attachments/assets/0da0535c-02ce-4720-8e39-b303147629ed)

 
ls file1
## OUTPUT
![Screenshot 2025-05-11 220228](https://github.com/user-attachments/assets/eb25f315-072a-4a83-855b-df5bfea49182)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot 2025-05-11 220302](https://github.com/user-attachments/assets/e30e9404-d08c-46c3-a997-8af501f5b5b8)
 
abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-05-11 220327](https://github.com/user-attachments/assets/a52e8e83-cc32-4fd6-a42b-fc30ccf0ddee)


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

![Screenshot 2025-05-11 220434](https://github.com/user-attachments/assets/fa2069de-a145-40b7-be7b-a1620a3f0709)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2025-05-11 220509](https://github.com/user-attachments/assets/dc6d3f56-f70a-4951-ac97-1456ce9722eb)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![Screenshot 2025-05-11 220539](https://github.com/user-attachments/assets/0bbf6715-53bf-442f-bcb8-f8af7b3b6d40)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![Screenshot 2025-05-11 220607](https://github.com/user-attachments/assets/30e4cd53-b771-4b2a-800e-4ceceb002ec9)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![Screenshot 2025-05-11 220641](https://github.com/user-attachments/assets/d5aa9be9-1566-4ff2-91d8-764bc2f305c7)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![Screenshot 2025-05-11 220705](https://github.com/user-attachments/assets/5774eb6d-adaa-430e-a07b-f9504dc2369c)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

![Screenshot 2025-05-11 220731](https://github.com/user-attachments/assets/36290918-9951-4e90-ab9c-8bed30680603)

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![Screenshot 2025-05-11 220859](https://github.com/user-attachments/assets/9d8d1018-9333-4c91-8f5f-9f4b1e4ae7a6)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 ![Screenshot 2025-05-11 221153](https://github.com/user-attachments/assets/3a3104f7-dbc3-4c2f-9a54-24adaaa27df8)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
![Screenshot 2025-05-11 221232](https://github.com/user-attachments/assets/c543475b-adfe-4f4c-9270-cd92cf5a8534)
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
![Screenshot 2025-05-11 221302](https://github.com/user-attachments/assets/2740a107-428d-4e76-a669-a12b26c3731a)
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
![Screenshot 2025-05-11 221333](https://github.com/user-attachments/assets/509e8a7f-92d2-4587-a0b5-fbd9d24cc7a4)
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 ![Screenshot 2025-05-11 221505](https://github.com/user-attachments/assets/eebf2e02-97f2-4397-813e-1c9322a8dad1)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 ![Screenshot 2025-05-11 221531](https://github.com/user-attachments/assets/336702f7-333a-462b-8f92-838d5d764978)

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![Screenshot 2025-05-11 221655](https://github.com/user-attachments/assets/cdf0b788-3648-46a8-8cd9-6c2169581119)


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![Screenshot 2025-05-11 221728](https://github.com/user-attachments/assets/e9b4c5fa-2801-4b7b-8650-42913b00f880)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![Screenshot 2025-05-11 221808](https://github.com/user-attachments/assets/7f37ac46-313a-411b-8288-53e261f8248f)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![Screenshot 2025-05-11 221844](https://github.com/user-attachments/assets/2e789517-32f3-4dcc-ab05-63205c40ada7)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![Screenshot 2025-05-11 221916](https://github.com/user-attachments/assets/ff1978db-4a3e-49e5-aa56-ff9848cc2f9f)
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

![Screenshot 2025-05-11 221940](https://github.com/user-attachments/assets/faeed086-6ecb-4bcc-9144-6280402d3b32)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2025-05-11 222000](https://github.com/user-attachments/assets/c25d48f4-0650-4207-91a1-00dac95e7a85)


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
![Screenshot 2025-05-11 222034](https://github.com/user-attachments/assets/0a31d07d-5fca-4919-9ffc-de780422b3ad)
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
![Screenshot 2025-05-11 222105](https://github.com/user-attachments/assets/c3f6fafd-eca9-4902-bb13-9a004f259c0f)
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![Screenshot 2025-05-11 222129](https://github.com/user-attachments/assets/876ddad1-b0a5-458e-8aa2-3166bb3ec619)


# RESULT:
The Commands are executed successfully.
