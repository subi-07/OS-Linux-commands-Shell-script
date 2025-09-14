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
<img width="231" height="147" alt="image" src="https://github.com/user-attachments/assets/bca9a220-69a0-4353-86a2-8b1237e7c42e" />



cat < file2
## OUTPUT
<img width="225" height="163" alt="image" src="https://github.com/user-attachments/assets/27a17bdf-f2a8-425a-86a7-360a407b2247" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="370" height="72" alt="image" src="https://github.com/user-attachments/assets/484f8bd0-92dc-482c-b19f-3cf69a209c92" />

comm file1 file2
 ## OUTPUT
<img width="377" height="221" alt="image" src="https://github.com/user-attachments/assets/01f4e31a-bef9-4548-87df-af1cd88638f3" />

 
diff file1 file2
## OUTPUT
<img width="322" height="264" alt="image" src="https://github.com/user-attachments/assets/08e227e0-0fc2-4fc9-8d12-28e2a69bbe03" />


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

<img width="286" height="100" alt="image" src="https://github.com/user-attachments/assets/528be3a7-49d7-47c5-b199-16750d4c037a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="353" height="124" alt="image" src="https://github.com/user-attachments/assets/5fa9b6d4-5141-41b8-a1ec-5c5925eefcd6" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="338" height="123" alt="image" src="https://github.com/user-attachments/assets/67c42559-ddc1-4b9b-89f5-8f6afc94c52f" />


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
<img width="288" height="74" alt="image" src="https://github.com/user-attachments/assets/169da6ee-fca8-482c-9489-e43d1fc89a4e" />



grep hello newfile 
## OUTPUT
<img width="281" height="72" alt="image" src="https://github.com/user-attachments/assets/a9fd4de4-d351-40b7-a6d7-c80fa62d9b66" />




grep -v hello newfile 
## OUTPUT
<img width="312" height="73" alt="image" src="https://github.com/user-attachments/assets/18d3d075-185f-4309-b684-c2e37750364b" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="370" height="100" alt="image" src="https://github.com/user-attachments/assets/3b0119b4-7cf9-4c9d-b1ec-7445c383b0ca" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="423" height="74" alt="image" src="https://github.com/user-attachments/assets/52004b7c-e44e-4968-bce3-58c1b9563a54" />



grep -R ubuntu /etc
## OUTPUT

<img width="1433" height="394" alt="image" src="https://github.com/user-attachments/assets/31bde3e7-931d-4e38-b061-1dc60ad070c4" />


grep -w -n world newfile   
## OUTPUT
<img width="329" height="89" alt="image" src="https://github.com/user-attachments/assets/f1148aab-f615-4e6b-91bc-3aed88817caa" />


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
<img width="395" height="94" alt="image" src="https://github.com/user-attachments/assets/ce159724-e7e8-4e18-b3d5-4fbda831d5ad" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="401" height="95" alt="image" src="https://github.com/user-attachments/assets/3dd7e5a9-8fb7-499c-be5a-25ffd126da1b" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="418" height="95" alt="image" src="https://github.com/user-attachments/assets/e016db2d-cbc8-40bd-a60e-3e219b86e37d" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="342" height="72" alt="image" src="https://github.com/user-attachments/assets/bbfce097-8dac-401a-8948-8cf7482cdbf4" />


egrep '(world$)' newfile 
## OUTPUT
<img width="334" height="100" alt="image" src="https://github.com/user-attachments/assets/c64ea05c-19d8-418c-99f3-f59bed67561c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="359" height="76" alt="image" src="https://github.com/user-attachments/assets/8878197c-ba6b-48e6-acd3-87243830f2ef" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="408" height="121" alt="image" src="https://github.com/user-attachments/assets/d3751dc1-82be-4c68-9f11-e75230f08377" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="367" height="71" alt="image" src="https://github.com/user-attachments/assets/b90121c2-f5a6-45f8-b76a-64c883efef7e" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="447" height="78" alt="image" src="https://github.com/user-attachments/assets/53c7bbe4-d53e-4c50-8fc0-d96fb076d18f" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="386" height="74" alt="image" src="https://github.com/user-attachments/assets/29c980f5-442e-4977-82c9-9baf0c9d8d53" />


egrep l{2} newfile
## OUTPUT
<img width="307" height="95" alt="image" src="https://github.com/user-attachments/assets/167facb3-2a58-44de-abf2-fcda22278e9f" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="386" height="123" alt="image" src="https://github.com/user-attachments/assets/7b6ce76b-369f-4e68-b476-c00366e9d00c" />


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
<img width="354" height="77" alt="image" src="https://github.com/user-attachments/assets/99ff4454-618b-4f40-b4d3-9242cb826e57" />



sed -n -e '$p' file23
## OUTPUT
<img width="368" height="74" alt="image" src="https://github.com/user-attachments/assets/a0b813a3-edaf-4aa5-87b3-7307d9255eb0" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="356" height="245" alt="image" src="https://github.com/user-attachments/assets/32fd35e9-46fb-4506-8fb6-fd166803692d" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="426" height="243" alt="image" src="https://github.com/user-attachments/assets/1e98251a-7b92-4387-b807-7fada627acbc" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="486" height="244" alt="image" src="https://github.com/user-attachments/assets/a670d99b-86f7-407b-b2b7-d2187e7f63cb" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="382" height="175" alt="image" src="https://github.com/user-attachments/assets/1615977e-c746-427c-80c2-a96cbe88b8ce" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="424" height="120" alt="image" src="https://github.com/user-attachments/assets/0924d9f7-1e8f-4485-97c2-43742719dda0" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="428" height="99" alt="image" src="https://github.com/user-attachments/assets/bb0e7e20-c93d-4c62-9e32-5a5fe5107059" />



seq 10 
## OUTPUT
<img width="298" height="293" alt="image" src="https://github.com/user-attachments/assets/a5324711-bad8-4eed-87cf-eb1d0cc5aff9" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="318" height="115" alt="image" src="https://github.com/user-attachments/assets/d32630f8-c62f-4730-a067-b915e9a8521b" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="363" height="116" alt="image" src="https://github.com/user-attachments/assets/31607fd4-8e9b-4f7f-8625-daf6de867193" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="339" height="143" alt="image" src="https://github.com/user-attachments/assets/14641376-5516-4682-bc12-26ba31ab2f5f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="300" height="118" alt="image" src="https://github.com/user-attachments/assets/c3f421ff-7536-42a3-b68f-c9d07e0856d8" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="356" height="115" alt="image" src="https://github.com/user-attachments/assets/f16075ee-0636-4297-b317-0b4093a76f0a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="417" height="122" alt="image" src="https://github.com/user-attachments/assets/a0b00f0f-2949-4906-bbee-fe43ef0a6118" />



sed -n '2,4{s/$/*/;p}' file23

<img width="421" height="125" alt="image" src="https://github.com/user-attachments/assets/c4a78c49-256c-4fd7-8e8c-2c2706ae3e3f" />


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
<img width="353" height="170" alt="image" src="https://github.com/user-attachments/assets/e6eb0ca7-b3ed-428d-b989-5f46414a201d" />



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
<img width="461" height="340" alt="image" src="https://github.com/user-attachments/assets/73b341ea-dee7-40bf-970b-9ee7ec607bbb" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="531" height="240" alt="image" src="https://github.com/user-attachments/assets/92791c98-bff9-48e9-92d5-04b53c15d267" />

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
<img width="388" height="123" alt="image" src="https://github.com/user-attachments/assets/39ce4a7f-824a-4c76-98e5-b07305313cbb" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="498" height="121" alt="image" src="https://github.com/user-attachments/assets/385f0a08-2110-4cbe-ab3a-038a41594013" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="579" height="403" alt="image" src="https://github.com/user-attachments/assets/19e0686e-3e03-45ea-81fe-07eb80314a78" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="972" height="504" alt="image" src="https://github.com/user-attachments/assets/06bb859d-4adb-4e40-aca9-4c2e2a4aadeb" />


tar -xvf backup.tar
## OUTPUT
<img width="550" height="433" alt="image" src="https://github.com/user-attachments/assets/1126231e-7026-41e6-9a42-07e9dc8fc941" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="405" height="76" alt="image" src="https://github.com/user-attachments/assets/79ea6121-9599-446a-8eb8-afb043fbe6a2" />

gunzip backup.tar.gz
## OUTPUT
<img width="1632" height="128" alt="image" src="https://github.com/user-attachments/assets/38b174d6-a012-4bf4-bbcc-e01081e65eb2" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="453" height="224" alt="image" src="https://github.com/user-attachments/assets/87e3bf8f-7adc-4a6f-b36c-9c28ce39e931" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="432" height="128" alt="image" src="https://github.com/user-attachments/assets/b1ec9192-1447-48c7-9db7-8fd3c08e009f" />


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
<img width="797" height="437" alt="image" src="https://github.com/user-attachments/assets/68284ad2-386c-406a-93c9-43b4e6621575" />

 
ls file1
## OUTPUT
<img width="293" height="74" alt="image" src="https://github.com/user-attachments/assets/f4d19cb4-e71b-40a0-a490-4426efccde1a" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="272" height="77" alt="image" src="https://github.com/user-attachments/assets/e8a0fe64-a345-4ea9-a647-4d1c7bf1e616" />

echo $?
## OUTPUT 

 <img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/3c3f2fe8-cd92-4c69-9cbd-272eb63f29e7" />

abcd
 
echo $?
 ## OUTPUT
<img width="361" height="71" alt="image" src="https://github.com/user-attachments/assets/9d0d8ce8-cbdf-4fd6-afdf-213cf4d077dc" />


 
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

<img width="432" height="257" alt="image" src="https://github.com/user-attachments/assets/437d183c-2fb8-4fd6-99de-fbaf17291233" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="692" height="152" alt="image" src="https://github.com/user-attachments/assets/ddc41915-50d9-4fff-b873-419239d64e87" />

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

<img width="651" height="212" alt="image" src="https://github.com/user-attachments/assets/f4f1e6c2-0ab7-4d71-838d-43880ed5b9e9" />

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

<img width="610" height="247" alt="image" src="https://github.com/user-attachments/assets/c7b432e8-bac2-42d9-ba4e-8bc736e1c8de" />


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

<img width="613" height="166" alt="image" src="https://github.com/user-attachments/assets/31226db2-855a-480a-95c3-f93a83a0f60a" />

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

<img width="690" height="193" alt="image" src="https://github.com/user-attachments/assets/d350447f-51ec-4b2b-8017-edd373c88ae6" />

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
<img width="702" height="152" alt="image" src="https://github.com/user-attachments/assets/4d3fd91f-20c2-4f3e-ba56-64cab2077be6" />


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
<img width="693" height="145" alt="image" src="https://github.com/user-attachments/assets/b189a1e0-00b3-44cc-a06a-9c246fa60b70" />

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
 ## Output
 <img width="357" height="117" alt="image" src="https://github.com/user-attachments/assets/f5d614cf-b50c-4b8f-a11c-c6ae90da3223" />

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
## Output
 <img width="366" height="339" alt="image" src="https://github.com/user-attachments/assets/1d18fe55-8db5-4426-9792-7fc7fae047d2" />

 
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
 ## Output
 <img width="527" height="171" alt="image" src="https://github.com/user-attachments/assets/7d5b02d5-c36d-41e7-9012-75ccb9695131" />

 
 
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
 ## Output
 <img width="658" height="242" alt="image" src="https://github.com/user-attachments/assets/657dc86e-adfd-470e-91dd-269432503327" />

 
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
## Output
 <img width="653" height="216" alt="image" src="https://github.com/user-attachments/assets/b31f806f-d83e-492e-a2b8-fbaecd460aea" />

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
 ## Output
 <img width="584" height="246" alt="image" src="https://github.com/user-attachments/assets/14d71048-0ed5-4310-9953-929e0ea2ad17" />

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

<img width="364" height="220" alt="image" src="https://github.com/user-attachments/assets/052e583f-b067-4cb0-91b0-3b59b8e640db" />


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

<img width="235" height="173" alt="image" src="https://github.com/user-attachments/assets/59ae4d93-39ba-4836-9ee6-44f59cd1d24f" />

 
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
<img width="369" height="224" alt="image" src="https://github.com/user-attachments/assets/a27f8da6-626b-4809-a42b-a5d0765cd1b0" />
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
<img width="323" height="387" alt="image" src="https://github.com/user-attachments/assets/7477327d-53cc-44ca-a5ee-1d1e4d13ebdb" />

 
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

 <img width="266" height="104" alt="image" src="https://github.com/user-attachments/assets/40347aeb-f838-4289-a5c6-290465640488" />


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
 <img width="331" height="178" alt="image" src="https://github.com/user-attachments/assets/69657555-406b-4006-baa0-f4bf9c5a97cf" />


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
<img width="389" height="105" alt="image" src="https://github.com/user-attachments/assets/071266b5-5577-4c81-9910-49d035475d17" />


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

 
<img width="400" height="107" alt="image" src="https://github.com/user-attachments/assets/e82cedd7-d93b-4530-82b3-3fd10a20b4e8" />


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

<img width="331" height="82" alt="image" src="https://github.com/user-attachments/assets/fd5162fb-81ea-4514-b27c-9024b5ae66c6" />

 
 ./funcex.sh 1 2

<img width="274" height="81" alt="image" src="https://github.com/user-attachments/assets/e4391bf5-4b31-44ab-aafd-0a13ff62dded" />

 
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

  <img width="335" height="122" alt="image" src="https://github.com/user-attachments/assets/df8dadad-8d19-4b4b-bfbf-97fb43062877" />
  
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

<img width="309" height="127" alt="image" src="https://github.com/user-attachments/assets/99167770-90a1-4a21-9acf-827c67e4ee9c" />


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
 
<img width="509" height="421" alt="image" src="https://github.com/user-attachments/assets/1db13d86-39af-40e2-a9fe-8024cfa1856c" />
 
 
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
 <img width="411" height="366" alt="image" src="https://github.com/user-attachments/assets/715dbc51-2db3-4f41-a0d4-48ba59a0535d" />

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
<img width="290" height="131" alt="image" src="https://github.com/user-attachments/assets/c87b04f6-2a8d-414f-a6a7-9e6e3f0c4660" />


# RESULT:
The Commands are executed successfully.
