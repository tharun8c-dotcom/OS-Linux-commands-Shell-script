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
<img width="806" height="223" alt="image" src="https://github.com/user-attachments/assets/df43dc69-2ea2-424d-b692-7c7f646cd4e1" />


cat < file2
## OUTPUT
<img width="994" height="237" alt="image" src="https://github.com/user-attachments/assets/654b8dbb-db0b-4297-a49f-27251030ba96" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="421" height="61" alt="image" src="https://github.com/user-attachments/assets/5139b64c-e684-4854-b0f3-6b0a021b91c1" />


comm file1 file2
 ## OUTPUT
<img width="1156" height="432" alt="image" src="https://github.com/user-attachments/assets/b8b92850-25f0-4377-9e76-09696b25ab7b" />

 
diff file1 file2
## OUTPUT
<img width="1147" height="407" alt="image" src="https://github.com/user-attachments/assets/34431937-9299-4585-a485-0c2328bf2544" />


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
<img width="870" height="162" alt="image" src="https://github.com/user-attachments/assets/b65a2aa8-59a7-4105-8060-250fe136e9ed" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="616" height="181" alt="image" src="https://github.com/user-attachments/assets/4714abd1-80a1-406e-8c2b-fadc5b7602bc" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="902" height="185" alt="image" src="https://github.com/user-attachments/assets/8e91e0b8-dc34-4b3c-ab2d-511825acd900" />


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
<img width="969" height="69" alt="image" src="https://github.com/user-attachments/assets/cc005870-4938-43fb-8cef-23c59b373d4a" />


grep hello newfile 
## OUTPUT
<img width="969" height="69" alt="image" src="https://github.com/user-attachments/assets/2756cf38-d062-4dbc-a21e-2de0681f3e67" />


grep -v hello newfile 
## OUTPUT

<img width="885" height="180" alt="image" src="https://github.com/user-attachments/assets/1c03f888-17dc-44e4-b4d9-4336826f41a5" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="736" height="96" alt="image" src="https://github.com/user-attachments/assets/2425cec8-4806-4335-b9f2-deed5fdddeb9" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="619" height="69" alt="image" src="https://github.com/user-attachments/assets/fd9322b0-3944-42ff-afb9-34d1d4d7da17" />


grep -R ubuntu /etc
## OUTPUT
![alt text](14.png)

grep -w -n world newfile   
## OUTPUT
<img width="1182" height="930" alt="image" src="https://github.com/user-attachments/assets/e176addd-0d86-4b04-9276-153b59774579" />

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
<img width="554" height="95" alt="image" src="https://github.com/user-attachments/assets/6bdd6469-8155-4d8f-9f93-2526c0209074" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="710" height="92" alt="image" src="https://github.com/user-attachments/assets/4e34fb3a-68b2-405d-84cf-fb93c48cd5f9" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="789" height="92" alt="image" src="https://github.com/user-attachments/assets/b8108eaf-8ee0-4277-ba2f-cc1a200f01c9" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="700" height="76" alt="image" src="https://github.com/user-attachments/assets/a8b3258a-9997-43ba-bef0-d70012aae2b9" />


egrep '(world$)' newfile 
## OUTPUT
<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/62cf5818-090b-4cd8-8771-0aec0d473198" />


egrep '(World$)' newfile 
## OUTPUT
<img width="645" height="95" alt="image" src="https://github.com/user-attachments/assets/cd7af792-f521-4a42-a713-a4016d6094ce" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="854" height="118" alt="image" src="https://github.com/user-attachments/assets/6d8835de-f6a0-4bbb-958f-f253760174be" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="864" height="74" alt="image" src="https://github.com/user-attachments/assets/ea0fb1da-3bcc-4dab-997f-64072d6e8a92" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="680" height="72" alt="image" src="https://github.com/user-attachments/assets/7fc82a9f-cb3c-4cec-8578-ba5e118ed9e0" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="726" height="68" alt="image" src="https://github.com/user-attachments/assets/3d6e2fd9-de5e-431c-883d-fab4a81d3e65" />


egrep l{2} newfile
## OUTPUT
<img width="768" height="96" alt="image" src="https://github.com/user-attachments/assets/1ae77ccd-069a-470d-b653-cbcf975c201f" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="769" height="120" alt="image" src="https://github.com/user-attachments/assets/a9b3e20c-ee7b-48ea-96dd-80636c9874a1" />


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
<img width="952" height="70" alt="image" src="https://github.com/user-attachments/assets/cd26e58d-4144-4a62-90ad-1c680549e86c" />



sed -n -e '$p' file23
## OUTPUT
<img width="781" height="72" alt="image" src="https://github.com/user-attachments/assets/15b9c02a-a925-4103-bb4c-d458bfd2f9da" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="665" height="96" alt="image" src="https://github.com/user-attachments/assets/3e8f3af3-69af-4fdc-9f41-5a367f337ea6" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="859" height="435" alt="image" src="https://github.com/user-attachments/assets/724a2daa-0eec-42cc-89f4-5dd8b22af239" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="730" height="415" alt="image" src="https://github.com/user-attachments/assets/7c5ceeff-32b6-41a2-9ffe-80fe71b3a667" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="666" height="169" alt="image" src="https://github.com/user-attachments/assets/800081e9-f1dc-4090-8a08-17a5b799166c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="762" height="182" alt="image" src="https://github.com/user-attachments/assets/8b867066-5c47-41cb-8fcf-0d2b8c210aa0" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="835" height="113" alt="image" src="https://github.com/user-attachments/assets/a2d0bdeb-30fa-40a9-94a4-41fef50a1d84" />


seq 10 
## OUTPUT
<img width="779" height="273" alt="image" src="https://github.com/user-attachments/assets/1df8a476-e821-45dd-9f89-6b7664f08fe2" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="942" height="122" alt="image" src="https://github.com/user-attachments/assets/78e7c276-d70b-4c3b-948e-a14fbdd5b1e4" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="764" height="117" alt="image" src="https://github.com/user-attachments/assets/95701571-2217-4e65-aabd-00ecf98ae946" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="679" height="139" alt="image" src="https://github.com/user-attachments/assets/33a10366-ee44-4a38-aaa4-fef3d14a3450" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="623" height="110" alt="image" src="https://github.com/user-attachments/assets/5582fa28-64cd-4037-ba94-0b7cb6458117" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="839" height="119" alt="image" src="https://github.com/user-attachments/assets/31681969-f22f-46d2-a0ea-5aeb82594c79" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="912" height="113" alt="image" src="https://github.com/user-attachments/assets/21cb83c3-95d1-4e54-b7e4-80386e498119" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="912" height="113" alt="image" src="https://github.com/user-attachments/assets/d1e202a5-53dc-45dd-986c-cfb32a131224" />


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
<img width="732" height="516" alt="image" src="https://github.com/user-attachments/assets/d4f88637-126c-4e7f-a1cc-beac54c82f35" />


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
<img width="812" height="567" alt="image" src="https://github.com/user-attachments/assets/b34885a3-d252-4559-a2a9-54ff6b3230bf" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="882" height="420" alt="image" src="https://github.com/user-attachments/assets/9caa4887-f581-4324-9094-f7ae7e5a4845" />


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
<img width="766" height="185" alt="image" src="https://github.com/user-attachments/assets/4f71114a-bb85-4372-b2b5-5b60cf01a4aa" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="883" height="193" alt="image" src="https://github.com/user-attachments/assets/2a8ad819-25c0-4db6-be46-d61a414571c6" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="926" height="632" alt="image" src="https://github.com/user-attachments/assets/6ea231b1-5075-48bc-a6dc-568ba7873f64" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1146" height="634" alt="image" src="https://github.com/user-attachments/assets/9808f753-79eb-458b-b203-0634944b240c" />


tar -xvf backup.tar
## OUTPUT
<img width="989" height="632" alt="image" src="https://github.com/user-attachments/assets/01d2a619-47a2-4fec-a6d1-5defcc989a3c" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="741" height="95" alt="image" src="https://github.com/user-attachments/assets/6ecbc943-ea56-40bf-b89d-9c29fd06f6b2" />


gunzip backup.tar.gz
## OUTPUT
<img width="1169" height="118" alt="image" src="https://github.com/user-attachments/assets/c6016573-1811-468d-90e0-7d332f0d08c0" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="872" height="233" alt="image" src="https://github.com/user-attachments/assets/19fbd32f-ff53-4ab2-aac4-0dcf3b792508" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="675" height="364" alt="image" src="https://github.com/user-attachments/assets/f3b56088-fcc5-492a-a624-ddfe5dbc7790" />


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
<img width="915" height="772" alt="image" src="https://github.com/user-attachments/assets/8d058905-b90c-426d-af59-2506934f47f0" />

 
ls file1
## OUTPUT
<img width="948" height="66" alt="image" src="https://github.com/user-attachments/assets/04c8ad52-bb08-422d-9555-bec9b08ec789" />


echo $?
## OUTPUT
<img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/9854dda5-090b-4c8e-8c41-79e3c7f3d3e2" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="790" height="77" alt="image" src="https://github.com/user-attachments/assets/24cb4b43-ea13-423a-8eb2-5e9a4f0a322d" />


abcd
 
echo $?
 ## OUTPUT
<img width="638" height="71" alt="image" src="https://github.com/user-attachments/assets/59719720-0f0b-4cd5-b882-5b076ea15d8f" />


 
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
<img width="1159" height="925" alt="image" src="https://github.com/user-attachments/assets/02468ae1-4226-45bf-810a-d99dca591c84" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="882" height="125" alt="image" src="https://github.com/user-attachments/assets/70113899-68ab-452d-861d-e4b80bc6223a" />


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
<img width="1160" height="746" alt="image" src="https://github.com/user-attachments/assets/1b602a08-df3d-4041-b4f2-6c3a73fd2651" />


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
<img width="1004" height="818" alt="image" src="https://github.com/user-attachments/assets/5b3152c3-5482-429d-8c4e-1434f4e57d81" />


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
<img width="814" height="378" alt="image" src="https://github.com/user-attachments/assets/60114e74-3cae-4b6a-9d39-da12c874713b" />


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
<img width="814" height="378" alt="image" src="https://github.com/user-attachments/assets/756b0a35-269b-4dbb-bc83-fd79495a72b1" />

<img width="1157" height="928" alt="image" src="https://github.com/user-attachments/assets/07e9f66b-d066-4dcf-a7de-e66dffa43d43" />


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
<img width="1160" height="928" alt="image" src="https://github.com/user-attachments/assets/b5ed0a64-a5f0-486f-9631-11e9d3bd9279" />


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
<img width="1084" height="454" alt="image" src="https://github.com/user-attachments/assets/e0244418-4055-4169-a679-5eeb44ef908a" />


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
## OUTPUT
<img width="970" height="638" alt="image" src="https://github.com/user-attachments/assets/78631301-15df-4feb-b927-597bd394fff8" />


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
<img width="895" height="411" alt="image" src="https://github.com/user-attachments/assets/aad92e94-7567-4053-97b7-12f005ea9ade" />

 
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
 <img width="884" height="545" alt="image" src="https://github.com/user-attachments/assets/dcb56f22-7f85-4dc8-af92-23e331536200" />

 
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
 
<img width="771" height="812" alt="image" src="https://github.com/user-attachments/assets/bba32771-fae7-4f2d-9485-1007595bf47b" />


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
 <img width="771" height="812" alt="image" src="https://github.com/user-attachments/assets/e0ad5db4-d7ac-445c-823e-6afe2f355f7c" />


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
 <img width="700" height="311" alt="image" src="https://github.com/user-attachments/assets/75f20f20-7f30-4f3e-b6fb-703adcf635b1" />

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
 <img width="1193" height="511" alt="image" src="https://github.com/user-attachments/assets/47d4723e-151b-4de3-bb0c-dc8ed27b6711" />


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

<img width="727" height="286" alt="image" src="https://github.com/user-attachments/assets/1b172ea2-2d37-451b-97e3-8ab3e85ce572" />


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
<img width="717" height="286" alt="image" src="https://github.com/user-attachments/assets/225e1da8-d105-4b7a-9231-b0bd867023ba" />


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

<img width="717" height="286" alt="image" src="https://github.com/user-attachments/assets/3353925f-c0b5-4caa-a13a-b7e4057f2bae" />

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



$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
## OUTPUT

![image-75](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/978f2ab3-ba04-442a-b668-62aa2450402e)


cat forcontinue.sh 
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

![image-76](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/cd016d47-b62c-4697-8211-2ccbb4e91301)

 
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
![image-77](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/25960989-f3d5-4a74-9eeb-ad4e77ea6755)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT

![image-78](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/33663a39-1b90-46dc-a249-29cce8e18d43)



 
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
![image-79](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/a353a7b2-7b6e-447f-99d8-eff19742bb64)



 
 ./funcex.sh 1 2
 ## output:
![image-80](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/c1b2d17b-036c-4d8b-b615-a4ae510d1db3)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT

![image-81](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/dc93f107-da58-4069-8676-fa8001a53772)

 
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

![image-82](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/e260570a-740d-40d6-b3d0-650cf1e0bfe6)

 
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
![image-85 (copy)](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/22c9f9e9-ae69-4152-9768-0122fe2f2a21)

 
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
 
![image-84](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/538413e2-0bfb-498f-bd90-181bb3e71a69)


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

![image-86](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/736ba1b8-9102-4b04-bf53-666e03ad5961)


# RESULT:
The Commands are executed successfully.
