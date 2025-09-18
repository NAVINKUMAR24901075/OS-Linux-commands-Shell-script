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

<img width="663" height="159" alt="image" src="https://github.com/user-attachments/assets/eeeef0e0-11cf-4e15-af17-fea36b1878b3" />

cat < file2
## OUTPUT

<img width="673" height="172" alt="image" src="https://github.com/user-attachments/assets/54dabfdf-751f-4a0a-95bf-7eccdf086d3a" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="632" height="79" alt="image" src="https://github.com/user-attachments/assets/6be99fbd-5eb8-4a49-a209-e061b19ffc1b" />
 
comm file1 file2
 ## OUTPUT
 
<img width="672" height="223" alt="image" src="https://github.com/user-attachments/assets/b99b37b9-ab9f-4366-af09-b7c74a794137" />
 
diff file1 file2
## OUTPUT

<img width="698" height="278" alt="image" src="https://github.com/user-attachments/assets/2601d692-c782-49d0-b644-ebb0808cfaab" />

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

<img width="663" height="107" alt="image" src="https://github.com/user-attachments/assets/95d2033f-1e97-476f-ab59-92057e0b7c88" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="611" height="126" alt="image" src="https://github.com/user-attachments/assets/40c6bc6a-87a3-480f-89bc-94bee3794f51" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="661" height="129" alt="image" src="https://github.com/user-attachments/assets/bc7352f4-5a83-4ccb-b0a4-70a7b48a3f13" />

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



grep hello newfile 
## OUTPUT

<img width="629" height="73" alt="image" src="https://github.com/user-attachments/assets/7cffb0a3-f548-4d2b-8019-cd1c9f085190" />

grep -v hello newfile 
## OUTPUT

<img width="630" height="80" alt="image" src="https://github.com/user-attachments/assets/fc62470a-1d49-40d9-b35f-847e8f736287" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="630" height="105" alt="image" src="https://github.com/user-attachments/assets/fc49aa39-227b-4218-a061-f461ba4e183f" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="614" height="73" alt="image" src="https://github.com/user-attachments/assets/a5e89ecc-f6ce-44d3-876f-2025515137a1" />

grep -R ubuntu /etc
## OUTPUT

<img width="1245" height="348" alt="image" src="https://github.com/user-attachments/assets/71815a9d-7245-4cbf-8885-6cadba89cd8c" />

grep -w -n world newfile   
## OUTPUT

<img width="647" height="99" alt="image" src="https://github.com/user-attachments/assets/58363799-a5a2-46d2-853d-577ad1131a14" />

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

<img width="614" height="109" alt="image" src="https://github.com/user-attachments/assets/d3ba0685-0c72-4725-bb5e-fcbd7533e3d2" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="632" height="102" alt="image" src="https://github.com/user-attachments/assets/df5e3ff5-88f0-482d-84bc-5a253deb61c8" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="649" height="101" alt="image" src="https://github.com/user-attachments/assets/5375e10d-154a-4f30-83dc-f0b9ef8bedc2" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="659" height="82" alt="image" src="https://github.com/user-attachments/assets/ca95a3c3-505b-4dbc-a2a7-199cb6e8f18f" />

egrep '(world$)' newfile 
## OUTPUT

<img width="642" height="107" alt="image" src="https://github.com/user-attachments/assets/08ecfba0-cab8-416b-832a-c6a63ce576c9" />

egrep '(World$)' newfile 
## OUTPUT

<img width="605" height="76" alt="image" src="https://github.com/user-attachments/assets/ddff417f-859f-4d77-91f5-eb6c74430c74" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="641" height="130" alt="image" src="https://github.com/user-attachments/assets/303099d2-c1d5-4bc7-bd58-b1b3ac528069" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="646" height="79" alt="image" src="https://github.com/user-attachments/assets/9eac6ac4-ea08-4200-aa20-bf5e01277a2f" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="637" height="74" alt="image" src="https://github.com/user-attachments/assets/51a994f9-d76a-4f51-8f5e-aa69f0f55d3d" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="647" height="84" alt="image" src="https://github.com/user-attachments/assets/45d07387-0370-43a0-af09-aee057a7b277" />

egrep l{2} newfile
## OUTPUT

<img width="635" height="102" alt="image" src="https://github.com/user-attachments/assets/0ca4a100-f2fa-4cd1-bc7f-32d96e6063fa" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="639" height="122" alt="image" src="https://github.com/user-attachments/assets/14e06682-354d-4539-8b24-03c440f0c7b6" />

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

<img width="602" height="76" alt="image" src="https://github.com/user-attachments/assets/31ec1391-eb2d-4e0b-9f70-5d17a3a3984a" />


sed -n -e '$p' file23
## OUTPUT

<img width="638" height="78" alt="image" src="https://github.com/user-attachments/assets/0dff0759-a30e-4b78-b093-c8c8c864388d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="600" height="251" alt="image" src="https://github.com/user-attachments/assets/4f250ed1-fae1-4fcd-8dc3-6ccf8eb24069" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="633" height="249" alt="image" src="https://github.com/user-attachments/assets/4f8e1178-4191-45c3-a9de-2570b3f3e1da" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="628" height="245" alt="image" src="https://github.com/user-attachments/assets/73ea7259-9e91-42d4-b7ac-82d307f8b235" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="623" height="177" alt="image" src="https://github.com/user-attachments/assets/efec6dc6-a610-4118-904b-e3ab128e8a03" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="604" height="131" alt="image" src="https://github.com/user-attachments/assets/168574e9-ee1f-4c2b-ad0b-e37b8cf45a3f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="612" height="101" alt="image" src="https://github.com/user-attachments/assets/58696285-ae02-4860-9629-8b30e678993c" />



seq 10 
## OUTPUT

<img width="621" height="301" alt="image" src="https://github.com/user-attachments/assets/0e1a144b-4aea-4108-a9e6-45c21d977c96" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="614" height="129" alt="image" src="https://github.com/user-attachments/assets/709a9044-2a3d-4bb4-b53a-6caae9c074d3" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="615" height="120" alt="image" src="https://github.com/user-attachments/assets/ca1fe640-c71e-4d68-aabb-8670eb32e90f" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="633" height="159" alt="image" src="https://github.com/user-attachments/assets/e5fbfb65-310c-4213-86c2-79ecfa6fc69b" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="638" height="127" alt="image" src="https://github.com/user-attachments/assets/0ad7d567-0848-4f80-bb18-cee593f26fd8" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="620" height="137" alt="image" src="https://github.com/user-attachments/assets/8ad4cdb8-6e0f-4f21-8d68-a7e697acfe39" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="638" height="136" alt="image" src="https://github.com/user-attachments/assets/1c365449-0dc6-4d23-8713-9a6f1d37e23b" />


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

<img width="644" height="180" alt="image" src="https://github.com/user-attachments/assets/fdcaae27-6d9f-4148-8ee5-6b9264769b98" />


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

<img width="652" height="183" alt="image" src="https://github.com/user-attachments/assets/c126223c-3a5c-407f-b85e-d834c37eaa73" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
<img width="623" height="257" alt="image" src="https://github.com/user-attachments/assets/71335a43-a45d-4f0b-9326-ec414b9baaa1" />


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
 
<img width="617" height="130" alt="image" src="https://github.com/user-attachments/assets/c50f267b-850a-46b3-b452-0c8ebb1db7c6" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="626" height="129" alt="image" src="https://github.com/user-attachments/assets/847356a1-9e8a-4870-ae09-0a3ca8433a80" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="635" height="304" alt="image" src="https://github.com/user-attachments/assets/21053dc2-dcae-45a6-bcec-971760b7777b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="721" height="306" alt="image" src="https://github.com/user-attachments/assets/d5992439-7b32-46f2-8123-3a38289f0382" />


tar -xvf backup.tar
## OUTPUT

<img width="714" height="307" alt="image" src="https://github.com/user-attachments/assets/06b05e4b-4f53-42c6-825c-33dba25354f8" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="714" height="80" alt="image" src="https://github.com/user-attachments/assets/301e5496-24d5-42b6-88cb-53ca3f99d808" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="741" height="56" alt="image" src="https://github.com/user-attachments/assets/59cc5eb8-e00b-4735-81d1-fe4d324eeb70" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="788" height="226" alt="image" src="https://github.com/user-attachments/assets/4a0b3cea-f195-4110-95fc-c1609b4f6453" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="711" height="125" alt="image" src="https://github.com/user-attachments/assets/5185d8d0-cd52-4a9a-b2b6-c611efbd3a8b" />


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

<img width="755" height="372" alt="image" src="https://github.com/user-attachments/assets/93efbf75-41d8-4182-ab08-a5a7e8122d40" />


 
ls file1
## OUTPUT

<img width="729" height="92" alt="image" src="https://github.com/user-attachments/assets/d9ccdc5f-b2eb-4f98-abb3-9698691a7949" />

echo $?
## OUTPUT

<img width="697" height="86" alt="image" src="https://github.com/user-attachments/assets/fc2c8faa-5657-4282-bdab-c9ddc7d9e5ba" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="697" height="86" alt="image" src="https://github.com/user-attachments/assets/2cdace54-2a04-4fe7-bddb-17d7251e02d3" />
 
abcd
 
echo $?
## OUTPUT

<img width="803" height="162" alt="image" src="https://github.com/user-attachments/assets/6d09fbac-0c0a-4a83-9783-e00169a3526b" />

 
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

<img width="743" height="321" alt="image" src="https://github.com/user-attachments/assets/3f5bff14-8af2-4c04-829f-9096fa715ae8" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="754" height="163" alt="image" src="https://github.com/user-attachments/assets/6da54a24-57d8-4b49-8c01-ab6da3935eda" />


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

<img width="727" height="111" alt="image" src="https://github.com/user-attachments/assets/9ecb88e4-a0e4-4eed-a162-94f556e96668" />


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

<img width="713" height="157" alt="image" src="https://github.com/user-attachments/assets/be65ddb4-8a09-4f15-ba1f-6c4ae09c9129" />



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

<img width="736" height="138" alt="image" src="https://github.com/user-attachments/assets/f36958fa-d624-407e-844e-3d4626200dd4" />


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

<img width="717" height="154" alt="image" src="https://github.com/user-attachments/assets/1c40c252-531e-4c74-a9d6-c5d11baf20a3" />

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

<img width="768" height="109" alt="image" src="https://github.com/user-attachments/assets/2648adb2-2ec6-415a-84e2-b659b4a4cedf" />


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

<img width="712" height="114" alt="image" src="https://github.com/user-attachments/assets/9b30f6c4-0656-46fe-9f6f-6594345227b6" />

# using the case command
cat > casecheck.sh 
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
 #OUTPUT
 
 <img width="725" height="83" alt="image" src="https://github.com/user-attachments/assets/f05b575d-3d18-4ba5-86fb-1e6c2b4173bc" />

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
#OUTPUT

 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
