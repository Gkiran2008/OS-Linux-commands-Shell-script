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

![{F61290FE-D294-489A-93C0-BFAFAC84B0D1}](https://github.com/user-attachments/assets/45a446a2-53f1-4472-822a-70dd5b4ca03e)


cat < file2
## OUTPUT

![{A37C60DA-E89B-497E-97C2-39AD4877B20A}](https://github.com/user-attachments/assets/272a245c-0bb3-49fb-84bf-7f320732b6ca)


# Comparing Files
cmp file1 file2
## OUTPUT

![{57C395AE-F0B2-442C-AC78-95D81F55CE6F}](https://github.com/user-attachments/assets/6cacbc31-6a84-482b-b92b-43b823f740a5)

 
comm file1 file2
 ## OUTPUT

![{4CEFBB4C-53E5-4987-A6F3-73C0897378AE}](https://github.com/user-attachments/assets/4e7732ce-e3bb-405b-b971-5289fa43d4e4)

 
diff file1 file2
## OUTPUT

![{D75766C1-6B45-4235-8778-9E122F016F41}](https://github.com/user-attachments/assets/ab9bf408-59d9-484f-b092-b16694eeee2d)



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

![{27F4A7EF-7441-4938-8CDB-E898B068DA50}](https://github.com/user-attachments/assets/8538af94-3bc6-4c83-8bd2-71db68057d52)



cut -d "|" -f 1 file22
## OUTPUT

![{807FF7DA-11D4-43BF-B712-440068278E17}](https://github.com/user-attachments/assets/82fa79a3-7747-454b-b52f-29fc86326237)


cut -d "|" -f 2 file22
## OUTPUT

![{909768DD-6DF9-49C1-8F00-945B51AF7B9E}](https://github.com/user-attachments/assets/4b5de542-e916-41da-bcdd-8a6d6c7c967a)


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![{5CEB3737-A126-451C-8232-DC8E20FA4836}](https://github.com/user-attachments/assets/0e53158d-b3ee-4642-abd0-9a9786e3e07f)


grep hello newfile 
## OUTPUT

![{ED9B40F3-94F1-4191-82C6-73710B76D0F3}](https://github.com/user-attachments/assets/36d7a62c-754e-4188-a10e-af4f7267ab3b)



grep -v hello newfile 
## OUTPUT

![{055562BA-759A-48CC-B766-DE06DA2667B1}](https://github.com/user-attachments/assets/5c8386ad-0c40-4c59-b796-872d26151b36)


cat newfile | grep -i "hello"
## OUTPUT

![{9C16C4ED-C5AC-4D65-A8A8-A0C78E83E64B}](https://github.com/user-attachments/assets/cef1716d-fdf0-435b-91f3-25c48b9af8e1)



cat newfile | grep -i -c "hello"
## OUTPUT

![{E040F84E-F702-48ED-81C9-852FBD8206D9}](https://github.com/user-attachments/assets/0ed122f5-15ab-4621-91d7-8c51781a5c60)



grep -R ubuntu /etc
## OUTPUT








grep -w -n world newfile   
## OUTPUT


![{568C246C-98D6-41BA-8215-5364985B6588}](https://github.com/user-attachments/assets/54e6eee8-88de-4248-aefd-0c4d0b4a970d)




cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
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

![{9615363A-949A-47C4-8796-43AFEC137455}](https://github.com/user-attachments/assets/2a575514-9b66-4c1f-8908-11c291d48ee3)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![{9E2A3F68-F260-4267-B401-2CC49101976F}](https://github.com/user-attachments/assets/5daa7f4f-2316-4083-92a3-1fe6fcf5a189)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![{2E18665D-02B1-4EA3-A8D1-465326197587}](https://github.com/user-attachments/assets/2ab24bac-f0b1-4029-8161-f4c7b921c173)



egrep '(^hello)' newfile 
## OUTPUT

![{A4962B1B-25F5-438D-9ADE-53BD5E78ECB9}](https://github.com/user-attachments/assets/6c86c926-d25e-41d2-a016-8f901d19b99c)



egrep '(world$)' newfile 
## OUTPUT


![{5FE62362-F6FA-4F25-AE20-B9E05E193C96}](https://github.com/user-attachments/assets/6ed33e04-679d-498d-a8f9-2926c32c2fe4)




egrep '(World$)' newfile 
## OUTPUT

![{C19C01A7-EC96-46C1-836B-6BBAD15D9D71}](https://github.com/user-attachments/assets/62436884-6cce-4f44-9316-66dc42a0ec57)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![{2A5874D3-511F-47A6-815E-4DD61D6B0A71}](https://github.com/user-attachments/assets/57dab454-7864-4d14-97a7-3c2fd1806372)




egrep '[1-9]' newfile 
## OUTPUT

![{1149F57D-5221-4140-8CF6-ED281E23DFD0}](https://github.com/user-attachments/assets/282dbfcd-7d77-4c24-aa02-537441d5f20d)


egrep 'Linux.*world' newfile 
## OUTPUT


![{1804D56B-DDBD-4B82-9A2A-B65D243D60F1}](https://github.com/user-attachments/assets/327f8745-cd60-4f30-88c9-8e60e86d5fc0)



egrep 'Linux.*World' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/14b3e2fd-96e0-4588-8770-e5fd774549fa)


egrep l{2} newfile
## OUTPUT

![{F52F5711-A817-42B8-81C3-E41847223B2D}](https://github.com/user-attachments/assets/b9f74482-5203-4d25-976e-71846bb4a67f)


egrep 's{1,2}' newfile
## OUTPUT 


![{50E01924-92A4-446C-A097-E0A717A9FE03}](https://github.com/user-attachments/assets/0092451f-8bc8-45bd-b2b9-ff793660cf08)



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

![{8313D674-54C5-49B0-8515-95630731BD59}](https://github.com/user-attachments/assets/dbaf7bea-545b-4ce1-bed5-db4ca68adc96)


sed -n -e '$p' file23
## OUTPUT

![{194BA3B9-2A34-4A09-B9D4-86329888BB56}](https://github.com/user-attachments/assets/41c746e8-ff0e-458a-8e9f-6ceed8e74313)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![{C5A30E23-6F72-4976-8EB5-CB021BC9DC84}](https://github.com/user-attachments/assets/4951592b-99f1-4d47-9570-9961e22d1af3)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![{5F63C02D-5070-4A7A-972B-057D9146932A}](https://github.com/user-attachments/assets/3efc57cd-f79d-47f9-8479-f59dc119ef52)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![{4D566A69-BF67-4C0C-9C7A-591609462C77}](https://github.com/user-attachments/assets/edf13f20-19fe-45e4-8483-20fc83c6878e)



sed -n -e '1,5p' file23
## OUTPUT

![{E9E6291A-5AEA-44B5-8407-36E81338F0BD}](https://github.com/user-attachments/assets/e0cf8edb-9ee5-4d83-85f6-a6a8f1f86287)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![{B7686AB4-99A0-4F73-A502-60DEEE48EEC7}](https://github.com/user-attachments/assets/da83b270-b24b-4de2-abe8-d74e32fa1812)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![{50C826AA-D665-43DB-8DE0-8A2B8119CEA2}](https://github.com/user-attachments/assets/713c8300-e266-462f-b7ff-6cc0ad5614aa)


seq 10 
## OUTPUT

![{D057A826-9AFB-49CB-8E2F-FC5AA1500702}](https://github.com/user-attachments/assets/d10e1ffd-dfd6-4d24-8bdf-e8454203ee64)


seq 10 | sed -n '4,6p'
## OUTPUT

![{9C4BBEF7-6233-4D37-AC68-DED19EA07B32}](https://github.com/user-attachments/assets/3ddc71e8-0581-4574-bede-434a4806cb3b)


seq 10 | sed -n '2,~4p'
## OUTPUT

![{C180224F-EC18-4CD4-98AA-88F5EC574CDC}](https://github.com/user-attachments/assets/23f54d33-ef41-4e1f-bed9-99ec63dd8372)


seq 3 | sed '2a hello'
## OUTPUT

![{1450FAF2-4E08-4F54-AC32-4CD06B20364C}](https://github.com/user-attachments/assets/4993b72e-2617-4734-8f48-650dbc3dffb4)


seq 2 | sed '2i hello'
## OUTPUT

![{7A1CE9DE-FA36-44F8-8348-F4E00B10B8C6}](https://github.com/user-attachments/assets/ad7aa994-9223-4991-b3c0-9b09ed45a08b)


seq 10 | sed '2,9c hello'
## OUTPUT

![{D49B6805-1EB3-49A1-8958-1180C97576E6}](https://github.com/user-attachments/assets/828dca04-68f3-43d5-8d67-fbe871c7ed02)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![{F78F4054-FDA6-4DC7-9D95-6C30E7F56DD8}](https://github.com/user-attachments/assets/848bbb78-10ac-45ab-bc60-65b9ece1ed13)


sed -n '2,4{s/$/*/;p}' file23

![{D07FB111-3F6E-4F13-93C0-136A2370CD19}](https://github.com/user-attachments/assets/21e74247-3aa0-4777-995d-8b073e75d8e9)


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

![{4C23494C-5152-4945-A3C3-50C6BD12C0F9}](https://github.com/user-attachments/assets/9716b8b5-66ac-4ed5-8b80-8ec4c5fb4fe5)


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

![{D906088F-FB42-4AED-83FF-1A2D0FA27D55}](https://github.com/user-attachments/assets/a0ba6d1b-5a97-4d33-8555-bdd287dc4675)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![{9E34A979-90C2-442D-B685-8C440206D250}](https://github.com/user-attachments/assets/4cf093ea-8bab-49a1-a972-2ed70c59f200)

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

![{FCDE3280-14CE-466A-8C8C-95784E094CF7}](https://github.com/user-attachments/assets/c04e4f42-acff-44e6-a558-f1a83271aca4)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![{8858A705-5F18-42B9-91A7-1053D2B6E73D}](https://github.com/user-attachments/assets/2130aa13-210b-467b-9991-ed57f4e820f1)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![{463C6A23-32B2-45DD-8E04-D89577CCECFE}](https://github.com/user-attachments/assets/5e64b391-2ccb-4fff-8094-4824cedcc8b9)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![{B832D31C-F858-4796-B6DB-1D6F88BB7865}](https://github.com/user-attachments/assets/971798ce-0c2a-412b-858e-a5de62b92cb4)



tar -xvf backup.tar
## OUTPUT

![{2365E49F-15AB-4107-81CF-BA49A53898D6}](https://github.com/user-attachments/assets/487d1718-1a77-4a9f-be04-7039374a3c78)


gzip backup.tar

ls .gz
## OUTPUT

![{62BE3A61-1F82-4E3F-AA9B-11781D0EC646}](https://github.com/user-attachments/assets/0176c8d2-0594-4a95-9050-73cb37a40dd4)


 
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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


# RESULT:
The Commands are executed successfully.
