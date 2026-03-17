# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

## Developed By: Infant Maria Stefanie .F
## Register Number: 212224230095

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

<img width="583" height="312" alt="image" src="https://github.com/user-attachments/assets/298a6039-9958-4297-9a50-2651f4f8d7d8" />


cat < file2
## OUTPUT

<img width="751" height="212" alt="image" src="https://github.com/user-attachments/assets/db36a0b2-4678-4724-a73c-71c9c739b5c4" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="779" height="50" alt="image" src="https://github.com/user-attachments/assets/91aa8e97-e676-4f95-915a-b687eed0a041" />

 
comm file1 file2
 ## OUTPUT
 
<img width="763" height="223" alt="image" src="https://github.com/user-attachments/assets/facfbb47-0ec4-4d5d-a69d-eae258018ec2" />

 
diff file1 file2
## OUTPUT

<img width="771" height="43" alt="image" src="https://github.com/user-attachments/assets/46543e53-e6e8-45e0-8175-2506c0dd6a14" />


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

<img width="772" height="233" alt="image" src="https://github.com/user-attachments/assets/b513bdee-f47c-47d4-be09-7d15c00e889f" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="770" height="96" alt="image" src="https://github.com/user-attachments/assets/535652f7-000f-4d97-9e5e-902744acc5f6" />


cut -d "|" -f 2 file22
## OUTPUT


<img width="767" height="93" alt="image" src="https://github.com/user-attachments/assets/4e3a9306-baf8-4f20-b439-a7a88e0cbe51" />

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

<img width="727" height="176" alt="image" src="https://github.com/user-attachments/assets/8d5c194a-04a9-470a-99c2-c8fea5377c4b" />


grep hello newfile 
## OUTPUT

<img width="743" height="50" alt="image" src="https://github.com/user-attachments/assets/58586fbd-e788-4982-8164-072eaa707591" />



grep -v hello newfile 
## OUTPUT

<img width="743" height="47" alt="image" src="https://github.com/user-attachments/assets/55c5f5ef-1c74-4beb-aa00-b524cb334fab" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="888" height="72" alt="image" src="https://github.com/user-attachments/assets/ead6fcd5-82d1-479d-932c-42a4a31e5c4a" />





cat newfile | grep -i -c "hello"
## OUTPUT

<img width="900" height="41" alt="image" src="https://github.com/user-attachments/assets/0fafdc04-95aa-4dcd-9c66-892786d482ed" />



grep -R ubuntu /etc
## OUTPUT


grep -w -n world newfile   
## OUTPUT

<img width="940" height="71" alt="image" src="https://github.com/user-attachments/assets/36ccd161-8cb9-479a-84f0-7799c4086f87" />

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

<img width="933" height="65" alt="image" src="https://github.com/user-attachments/assets/3efe3a00-fba1-4108-86a1-802b41b19f19" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="937" height="71" alt="image" src="https://github.com/user-attachments/assets/9fc1abf4-a4b8-425b-bd68-6a3bb451f587" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="951" height="73" alt="image" src="https://github.com/user-attachments/assets/d8ca44b5-ed25-439d-908e-90e71556718d" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="932" height="48" alt="image" src="https://github.com/user-attachments/assets/0de6ec3d-16ca-4bb0-80cc-531fdb908814" />


egrep '(world$)' newfile 
## OUTPUT

<img width="932" height="48" alt="image" src="https://github.com/user-attachments/assets/2e736e9d-9b4d-4c54-aee6-2786b5554667" />


egrep '(World$)' newfile 
## OUTPUT

<img width="947" height="50" alt="image" src="https://github.com/user-attachments/assets/dae406b2-ea12-4f3b-b314-9f92bf290d9e" />




egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="950" height="87" alt="image" src="https://github.com/user-attachments/assets/bc8c05b2-22fa-4cfa-b888-421b7ca02aeb" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="942" height="50" alt="image" src="https://github.com/user-attachments/assets/887267ab-b548-4c60-93e5-8cb0e1b91104" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="943" height="48" alt="image" src="https://github.com/user-attachments/assets/12ad3e20-7eba-472b-bbdf-177dd9aa174f" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="950" height="52" alt="image" src="https://github.com/user-attachments/assets/094f16ba-91dc-468b-bc60-c5306c8ad315" />


egrep l{2} newfile
## OUTPUT

<img width="948" height="72" alt="image" src="https://github.com/user-attachments/assets/e0b9ad61-481d-4749-ab6a-1da2472fbb9a" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="923" height="85" alt="image" src="https://github.com/user-attachments/assets/405f172d-64d4-46fd-b0a3-d8654300c393" />


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

<img width="808" height="37" alt="image" src="https://github.com/user-attachments/assets/24be3536-ef2f-4fe3-a95c-c5d70571ceb1" />


sed -n -e '$p' file23
## OUTPUT

<img width="815" height="40" alt="image" src="https://github.com/user-attachments/assets/8b12c49b-8091-471d-8769-f25bf184c6ea" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="806" height="172" alt="image" src="https://github.com/user-attachments/assets/68370255-5465-4a44-9c96-c51758acc7b0" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="807" height="170" alt="image" src="https://github.com/user-attachments/assets/fe2834ff-7830-4385-a1e5-6e7beb6ca0f1" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="815" height="170" alt="image" src="https://github.com/user-attachments/assets/996a2467-e752-4443-9ec0-f025fdb754de" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="806" height="118" alt="image" src="https://github.com/user-attachments/assets/f94137b1-74d0-410c-87c3-b732237a8087" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="811" height="74" alt="image" src="https://github.com/user-attachments/assets/2546d226-35fc-4845-a353-712aa17ae885" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="806" height="58" alt="image" src="https://github.com/user-attachments/assets/9acefa23-8e79-4b59-ab75-babd68c72b11" />


seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="820" height="213" alt="image" src="https://github.com/user-attachments/assets/933ef53e-2f14-4d3c-8704-d4d80dad8eaa" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="772" height="77" alt="image" src="https://github.com/user-attachments/assets/e4188d82-f87e-4df1-87e4-8965486de159" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="793" height="97" alt="image" src="https://github.com/user-attachments/assets/6bad6580-d644-49ce-add4-6c634caa3883" />



seq 2 | sed '2i hello'
## OUTPUT


<img width="830" height="73" alt="image" src="https://github.com/user-attachments/assets/72e4b53a-7966-48d6-a7d7-701dcadc01e0" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="818" height="82" alt="image" src="https://github.com/user-attachments/assets/698233e7-cba1-49b3-988b-55d0975cecad" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="811" height="77" alt="image" src="https://github.com/user-attachments/assets/91266a4d-5e71-4c16-8d40-1e47a2720a3f" />


sed -n '2,4{s/$/*/;p}' file23

<img width="821" height="71" alt="image" src="https://github.com/user-attachments/assets/61a622d8-ca63-4f8b-8bb6-fc55c88876cc" />


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

<img width="813" height="257" alt="image" src="https://github.com/user-attachments/assets/60db6328-88f5-41e4-b19c-3fdc7430eb34" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="816" height="210" alt="image" src="https://github.com/user-attachments/assets/47698798-0951-450c-a499-a232190c28b2" />

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

<img width="807" height="82" alt="image" src="https://github.com/user-attachments/assets/6fe29991-6f8a-4889-8e3a-87b67ecdb85d" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="815" height="82" alt="image" src="https://github.com/user-attachments/assets/71cb78d7-07a1-4874-9a02-fe28157fad89" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="808" height="710" alt="image" src="https://github.com/user-attachments/assets/299a9b93-88fa-4fa0-8891-bab17bc2ea7f" />
<img width="808" height="615" alt="image" src="https://github.com/user-attachments/assets/c97a67cc-47f3-451d-bf4c-9668ab9d5320" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="810" height="917" alt="image" src="https://github.com/user-attachments/assets/5d9be34e-1012-4212-b828-dc2ea797134a" />

<img width="807" height="766" alt="image" src="https://github.com/user-attachments/assets/4cce5bbc-b090-41ae-a712-7084b81afa80" />

tar -xvf backup.tar
## OUTPUT

<img width="810" height="496" alt="image" src="https://github.com/user-attachments/assets/55938f3e-3a02-46ff-b84f-4596017b082d" />


gzip backup.tar

ls .gz
## OUTPUT

gunzip backup.tar.gz
## OUTPUT

 <img width="816" height="61" alt="image" src="https://github.com/user-attachments/assets/a32f1fb6-bc9b-41e8-bc15-a5093b5eb3ae" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="811" height="115" alt="image" src="https://github.com/user-attachments/assets/e3ea4c60-fbc0-4677-9635-80254a30fd2f" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="808" height="133" alt="image" src="https://github.com/user-attachments/assets/08f55255-eccf-4757-9c20-57573344ffa0" />


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

<img width="813" height="297" alt="image" src="https://github.com/user-attachments/assets/cb33554a-6cf1-45ab-bd02-a87c356f2887" />

 
ls file1
## OUTPUT

<img width="807" height="30" alt="image" src="https://github.com/user-attachments/assets/21ccadec-64f4-4efe-9673-15c9fe4ff643" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

<img width="808" height="22" alt="image" src="https://github.com/user-attachments/assets/5251a07a-96b5-4a88-958e-fa9f22ab8e40" />

echo $?
## OUTPUT 

<img width="810" height="30" alt="image" src="https://github.com/user-attachments/assets/a8495953-b5e0-4cdf-aebe-8fa23dc92b26" />

abcd
 
echo $?
## OUTPUT

<img width="810" height="30" alt="image" src="https://github.com/user-attachments/assets/ae2509a4-2ff6-4816-81b6-961da3fc5625" />

 
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

<img width="806" height="403" alt="image" src="https://github.com/user-attachments/assets/8c8ba84d-c856-4d56-a2c9-f1bcd606a577" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="810" height="107" alt="image" src="https://github.com/user-attachments/assets/c4afba68-104e-4a95-8fc3-81aec414aac9" />


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

<img width="807" height="170" alt="image" src="https://github.com/user-attachments/assets/161f99f7-c5ab-4f39-a49b-32fcaf75677d" />

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

<img width="810" height="373" alt="image" src="https://github.com/user-attachments/assets/28b779a2-61c7-48c9-b8e9-20c8453ba7d4" />


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

<img width="816" height="328" alt="image" src="https://github.com/user-attachments/assets/89e416ff-d539-4f9f-86ac-b23fb962cfe9" />

<img width="816" height="328" alt="image" src="https://github.com/user-attachments/assets/35b73299-4d1a-4e74-9b6f-8ea1b0725337" />

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

<img width="812" height="417" alt="image" src="https://github.com/user-attachments/assets/72bbdc24-c6d0-4944-9598-f946f8f4c7fa" />


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

<img width="817" height="217" alt="image" src="https://github.com/user-attachments/assets/9e907c20-f7eb-46be-87fc-762b1aa3a659" />


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

<img width="797" height="202" alt="image" src="https://github.com/user-attachments/assets/2bce3a16-ccc5-4c21-acba-1585732c1cee" />


# RESULT:
The Commands are executed successfully.
