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
<img width="341" height="102" alt="image" src="https://github.com/user-attachments/assets/587125a9-8c1c-45da-bbea-c095fc3104fb" />



cat < file2
## OUTPUT
<img width="328" height="162" alt="image" src="https://github.com/user-attachments/assets/0811359a-9f79-4585-98c5-ca6b71df95a8" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/3edf786d-eab1-4d90-91c3-2d2498de2172" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/47932edd-8c00-4d34-ac19-07abe7bd460c" />

 
diff file1 file2
## OUTPUT
<img width="428" height="305" alt="image" src="https://github.com/user-attachments/assets/80465c10-f6cf-4819-a0b7-8df9cf994ff2" />


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
<img width="383" height="84" alt="image" src="https://github.com/user-attachments/assets/d18a4c1e-a0e0-423e-921d-a467910ed987" />




cut -d "|" -f 1 file22
## OUTPUT


<img width="433" height="109" alt="image" src="https://github.com/user-attachments/assets/95faf39c-fba8-479e-99b9-805f9928c27e" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="image" src="https://github.com/user-attachments/assets/18bc9ea6-1e91-4ac2-97f1-690ec5673c44" />


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
<img width="409" height="56" alt="image" src="https://github.com/user-attachments/assets/9ab71426-75de-4571-b1ed-be321999b946" />



grep hello newfile 
## OUTPUT
<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/ac586df8-c687-4bda-83c6-2b4c906615ec" />




grep -v hello newfile 
## OUTPUT
<img width="430" height="59" alt="image" src="https://github.com/user-attachments/assets/98fcf859-7ab4-4577-8535-63ddf1455153" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/eb2b4b36-06e9-46bd-9e77-c0084b00b043" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="578" height="52" alt="image" src="https://github.com/user-attachments/assets/4fca4df2-a867-4f0d-b629-5a4b9e227a63" />




grep -R ubuntu /etc
## OUTPUT
<img width="609" height="218" alt="image" src="https://github.com/user-attachments/assets/88deb328-25c3-44a2-ab27-b4bf8e8ee16d" />



grep -w -n world newfile   
## OUTPUT
<img width="474" height="80" alt="image" src="https://github.com/user-attachments/assets/e86aa43a-3653-47b2-98fc-2327f12ada57" />


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
<img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/af285248-445b-4668-a22e-6e66a1950769" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/55ce23f0-de6e-4207-8c88-f5ff731462c3" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/8eddfc4a-513d-4feb-8c82-abfb156f003d" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/7200955b-4a50-4d06-ab78-22127b142cc4" />



egrep '(world$)' newfile 
## OUTPUT
<img width="495" height="54" alt="image" src="https://github.com/user-attachments/assets/0ef1cf87-c7d7-4098-a890-76eeda33d4c5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="485" height="49" alt="image" src="https://github.com/user-attachments/assets/5f59e640-1c56-4034-8e5c-03b8cd000d44" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="559" height="76" alt="image" src="https://github.com/user-attachments/assets/a5bc7806-4f3a-4c55-88d3-c4d44180e131" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="475" height="62" alt="image" src="https://github.com/user-attachments/assets/3add302e-49be-47ed-bef2-fab023097060" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="547" height="55" alt="image" src="https://github.com/user-attachments/assets/b3329102-f02f-4728-8b0e-44204f0b36f4" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="540" height="57" alt="image" src="https://github.com/user-attachments/assets/ba797182-802e-421f-8bec-f42d1e34445a" />

egrep l{2} newfile
## OUTPUT

<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/35fdd4cd-077b-4b8e-9d29-9ee6c226cb0e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="image" src="https://github.com/user-attachments/assets/d031d722-252f-4c40-9d07-b69de1248291" />


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
<img width="446" height="52" alt="image" src="https://github.com/user-attachments/assets/1b114615-50de-4e98-8f50-f029c121bf1b" />



sed -n -e '$p' file23
## OUTPUT
<img width="463" height="58" alt="image" src="https://github.com/user-attachments/assets/01e4b1da-2282-4571-97b6-b8ae611d6473" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="520" height="243" alt="image" src="https://github.com/user-attachments/assets/a7bff828-4a12-4e90-9214-334155dd71b4" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="521" height="237" alt="image" src="https://github.com/user-attachments/assets/238981d9-dc69-44c9-b91a-ea939da34dec" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="555" height="245" alt="image" src="https://github.com/user-attachments/assets/2ee82ce9-6e34-4e76-b135-d70f1abc6ca1" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="481" height="169" alt="image" src="https://github.com/user-attachments/assets/294c9a45-ec9b-459d-9451-3124c7613e83" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="520" height="108" alt="image" src="https://github.com/user-attachments/assets/5bd7b788-cd26-45f0-85ef-b9b7a85ce942" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/84041af0-7950-4a8a-b490-d65b20e5c460" />


seq 10 
## OUTPUT

<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/e00ac0fd-fe6a-472b-bb5c-a22f6534d17e" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/404ea3f5-5439-4385-b623-606fe6965007" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/749f22f6-6ec0-4e5b-9772-88b3b1a1a655" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/8781464a-3fc3-40e4-a9ee-b090b09c70e3" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/dfc45091-9787-4015-bb37-4ddfb0e1a58d" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/9515cdd7-9cfa-400e-aec1-83507cb7131a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/7eef71f8-14d4-408f-9ea9-c0e12ea19602" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="565" height="112" alt="image" src="https://github.com/user-attachments/assets/a1daeb0e-87c0-4e21-9f82-a392dd66805a" />



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
<img width="343" height="156" alt="image" src="https://github.com/user-attachments/assets/af9977bc-4c8e-4d79-b502-b1f17587bb00" />


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
<img width="363" height="160" alt="image" src="https://github.com/user-attachments/assets/5a4afe07-8f4f-403e-8567-2d93e7d41fad" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="652" height="243" alt="image" src="https://github.com/user-attachments/assets/aa73058b-c697-4333-a06b-1ada9743c067" />

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

<img width="536" height="113" alt="image" src="https://github.com/user-attachments/assets/923bc64b-095d-424c-8183-0f3033d9393a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/0a752653-147f-4256-b9d2-a659d24f6ce6" />


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
<img width="430" height="331" alt="image" src="https://github.com/user-attachments/assets/9ebfbd79-b7cf-42df-9cf5-a829128ee345" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/6ae085b3-2c51-4f61-b5ff-e9c76091dac0" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/f731a4ad-0302-45aa-a2b3-571a2539d873" />

echo $?
## OUTPUT 
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/97fa1bf2-b783-459d-a755-ff3fef614cee" />

abcd
 
echo $?
 ## OUTPUT
<img width="469" height="221" alt="image" src="https://github.com/user-attachments/assets/04e3418a-cd94-483b-a5ea-5a1b402e5391" />


 
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
## OUTPUT
<img width="476" height="243" alt="image" src="https://github.com/user-attachments/assets/0512a556-4464-45a8-a3df-fbe3ce88393f" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="image" src="https://github.com/user-attachments/assets/1f427478-2514-4025-8354-676af13ff905" />


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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/d9793b8c-e8ae-417a-97e1-cb25d01b4871" />

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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/8d8857fc-deb2-41b4-ba03-9dc43c3f734c" />



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
## OUTPUT
<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/e9e85b13-4fa5-4636-8dfc-3e2fb41b4933" />

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
## OUTPUT
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/7f90121b-dd35-4947-a8e9-c10dbfa6e377" />

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
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/cd703870-29c4-4e52-82c9-9ab96157ff5b" />


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
<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/ba3ccf3f-8354-4499-ad75-3ffc26113598" />

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
<img width="504" height="160" alt="image" src="https://github.com/user-attachments/assets/e46f2c5d-4ebc-4202-9b66-895756c46401" />

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
<img width="446" height="201" alt="image" src="https://github.com/user-attachments/assets/3032ea02-66ec-4787-8d16-04597ba437ee" />


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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/3543912a-cb9f-432b-8a1a-aa30cada3d0b" />

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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/85301548-a688-4890-97b4-d48e9a6ace78" />

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
<img width="412" height="201" alt="image" src="https://github.com/user-attachments/assets/eb314566-26d8-49d8-8c6f-63d977aa8b09" />

 
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
<img width="481" height="144" alt="image" src="https://github.com/user-attachments/assets/4504422a-729a-4329-b266-e5ca584c159e" />

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
<img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/704bf6fe-42fa-42e8-83ee-8f63813b4aa0" />

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

<img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/963862c2-093e-4efe-8a4b-8f09f9a48b24" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="774" height="137" alt="image" src="https://github.com/user-attachments/assets/3b2231d5-0a0e-4578-a5da-ca5ad21ada18" />


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

<img width="755" height="44" alt="image" src="https://github.com/user-attachments/assets/83e814c3-f549-41ec-b8a5-759c399a3ca5" />

 ./funcex.sh 1 2
 <img width="762" height="38" alt="image" src="https://github.com/user-attachments/assets/4b04abeb-cbf6-4072-9494-93364055c4ef" />

 
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
<img width="758" height="63" alt="image" src="https://github.com/user-attachments/assets/b0c6e5d8-bc13-4c07-a12d-49121a423797" />


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
<img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/b4c99bdc-b4fb-4cd5-a515-98c9b75aa890" />

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
 <img width="765" height="327" alt="image" src="https://github.com/user-attachments/assets/3c86ab39-4421-41e0-9b9b-86d096878370" />

 
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
 <img width="783" height="218" alt="image" src="https://github.com/user-attachments/assets/40b38e97-fa04-4872-b08c-6913bbf39921" />

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
<img width="772" height="70" alt="image" src="https://github.com/user-attachments/assets/089a8b85-8da4-47f9-a55f-7d48da4a770a" />


# RESULT:
The Commands are executed successfully.
