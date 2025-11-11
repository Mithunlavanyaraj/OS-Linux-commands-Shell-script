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
<img width="358" height="237" alt="exp1b" src="https://github.com/user-attachments/assets/ff984e2b-af25-4da7-ae35-e9bf9bc59d82" />




cat < file2
## OUTPUT
<img width="377" height="215" alt="exp1a" src="https://github.com/user-attachments/assets/ca0cd0da-df56-46eb-9992-b7c8873ec698" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="437" height="221" alt="exp1c" src="https://github.com/user-attachments/assets/dd6f6d9b-5a1d-4a7b-b373-afa2b541a45a" />

 
comm file1 file2
 ## OUTPUT
 <img width="412" height="282" alt="1d" src="https://github.com/user-attachments/assets/22887ace-c319-404d-8ad5-a0d53440a4a0" />


 
diff file1 file2
## OUTPUT
<img width="361" height="357" alt="1e" src="https://github.com/user-attachments/assets/7b5cc463-2133-4133-9cf0-6afbf48343ef" />



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

<img width="351" height="187" alt="1f" src="https://github.com/user-attachments/assets/cd24183f-208c-4ea5-9e5e-dfe5acb2158a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="328" height="193" alt="1g" src="https://github.com/user-attachments/assets/f15573b6-0838-43af-bd83-aaea687166c4" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="302" height="136" alt="1h" src="https://github.com/user-attachments/assets/67b3bfb6-0a77-422d-85f8-34168835f40a" />


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
<img width="318" height="132" alt="1i" src="https://github.com/user-attachments/assets/36333897-e956-47c8-938c-606514b1b2eb" />



grep hello newfile 
## OUTPUT

<img width="483" height="257" alt="1j" src="https://github.com/user-attachments/assets/b72b94cf-c513-443c-9f85-a043074889ec" />



grep -v hello newfile 
## OUTPUT
<img width="425" height="188" alt="1k" src="https://github.com/user-attachments/assets/b0251d4c-1f29-4f5a-96c7-a04d9137dbb0" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="798" height="573" alt="1l" src="https://github.com/user-attachments/assets/4922be0f-4164-4f1b-b6c7-24718422e0d0" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="347" height="152" alt="1m" src="https://github.com/user-attachments/assets/a5c4950d-1b8f-46a8-b01b-0eece01f7087" />


grep -R ubuntu /etc
## OUTPUT

<img width="373" height="281" alt="1n" src="https://github.com/user-attachments/assets/ed434b17-03f2-4f86-b623-0e948f18cf1b" />


grep -w -n world newfile   
## OUTPUT

<img width="495" height="235" alt="1o" src="https://github.com/user-attachments/assets/5bbbe382-77c8-4899-9c1b-1ed1067120cc" />

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

<img width="778" height="221" alt="1p" src="https://github.com/user-attachments/assets/6f4c1016-72fd-4e81-9841-f8da505a837e" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="452" height="207" alt="1q" src="https://github.com/user-attachments/assets/839a25b3-e48c-4d25-8165-7fdb35764a50" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="426" height="175" alt="1r" src="https://github.com/user-attachments/assets/6f25f2a8-6dbd-4e7b-b4a4-7284ba450d69" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="537" height="192" alt="1s" src="https://github.com/user-attachments/assets/d16bc6bb-e3ae-43db-968f-79483945258a" />


egrep '(world$)' newfile 
## OUTPUT

<img width="430" height="163" alt="1t" src="https://github.com/user-attachments/assets/be5c4e86-3185-41ff-a7b2-bc6cc44a2190" />


egrep '(World$)' newfile 
## OUTPUT
<img width="468" height="121" alt="1u" src="https://github.com/user-attachments/assets/da9ca650-94ca-48ac-b401-2e15a46d5b82" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="487" height="111" alt="1v" src="https://github.com/user-attachments/assets/5f7cc297-b400-4033-ac0d-22529ada6ac1" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="368" height="271" alt="1w" src="https://github.com/user-attachments/assets/6b122d67-bc07-4bbb-b887-05be9f6615fc" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="517" height="256" alt="1x" src="https://github.com/user-attachments/assets/972b6e62-12c8-4f59-902a-2290cad0c7df" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="408" height="282" alt="1y" src="https://github.com/user-attachments/assets/58cd151c-403c-4f84-8b98-149361bba43a" />


egrep l{2} newfile
## OUTPUT

<img width="296" height="81" alt="1z" src="https://github.com/user-attachments/assets/8f5c28ce-7791-42e8-b202-44787b8257ae" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="298" height="85" alt="1aa" src="https://github.com/user-attachments/assets/91303d1a-85e0-42ed-bd2e-074ad82e8dcf" />


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

<img width="342" height="76" alt="1bb" src="https://github.com/user-attachments/assets/377c850f-4f72-4b08-a502-f6e5777f8838" />


sed -n -e '$p' file23
## OUTPUT

<img width="363" height="258" alt="1cc" src="https://github.com/user-attachments/assets/69754342-326f-4042-a7bf-e0628b4a6435" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="377" height="208" alt="1dd" src="https://github.com/user-attachments/assets/40535716-9aa1-403c-9d80-525f712cbd09" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="376" height="131" alt="1ee" src="https://github.com/user-attachments/assets/ea4cca01-0f1c-45ee-bf7e-bc09fbb448ba" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="371" height="150" alt="1ff" src="https://github.com/user-attachments/assets/2e4e7ca9-43e9-4600-a2b4-f91f10f7bddf" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="332" height="305" alt="1gg" src="https://github.com/user-attachments/assets/0edc64cb-b7fa-4e18-983e-2b75dd351d1c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="336" height="131" alt="1hh" src="https://github.com/user-attachments/assets/8d5c46f0-1f63-424a-8513-a03290aadd4a" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="341" height="136" alt="1ii" src="https://github.com/user-attachments/assets/1132e984-9df5-4ce9-be07-f8032054875a" />


seq 10 
## OUTPUT

<img width="367" height="152" alt="1jj" src="https://github.com/user-attachments/assets/d8fdeeb2-ea5a-48f9-98f7-067aa8770e93" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="348" height="147" alt="1kk" src="https://github.com/user-attachments/assets/2f46e7d1-a8ea-486c-a4ce-e0c337ff7e31" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="385" height="137" alt="1ll" src="https://github.com/user-attachments/assets/41f9fea6-6505-4c8b-a99c-2550c786cf23" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="420" height="133" alt="1mm" src="https://github.com/user-attachments/assets/0334f9fd-5f24-4e6b-8732-020d9ff68200" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="423" height="141" alt="1nn" src="https://github.com/user-attachments/assets/e5e3c9d5-9cfe-498e-a971-b3c3d351448f" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="381" height="178" alt="1oo" src="https://github.com/user-attachments/assets/6d19c392-7be0-4111-8f3c-047a633d9a74" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="380" height="192" alt="1pp" src="https://github.com/user-attachments/assets/488035d9-e405-4724-87be-639a170457ba" />


sed -n '2,4{s/$/*/;p}' file23


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
<img width="453" height="206" alt="1qq" src="https://github.com/user-attachments/assets/db894a58-2cef-4e46-98a4-76326db2d92a" />


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

<img width="478" height="267" alt="1rr" src="https://github.com/user-attachments/assets/0a7d8466-a8d0-48fd-9037-1b6a317d7a71" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="343" height="138" alt="1ss" src="https://github.com/user-attachments/assets/4b8e18dc-afd5-45a8-b150-44bc8244b6ee" />

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
<img width="360" height="135" alt="1tt" src="https://github.com/user-attachments/assets/9a78b4c6-6523-4da4-996a-448d76c7385c" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="403" height="807" alt="1uu" src="https://github.com/user-attachments/assets/fdc006d9-a96c-4000-8bdf-def289c823a5" />


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
<img width="582" height="277" alt="1vv" src="https://github.com/user-attachments/assets/149456a6-15ea-470c-95bb-a13d9a0efd34" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="355" height="130" alt="1ww" src="https://github.com/user-attachments/assets/d035b3e1-d359-4a42-a57b-f3852b3edf54" />


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
<img width="440" height="327" alt="1xx" src="https://github.com/user-attachments/assets/76009e64-ea92-40bb-b8ab-600d840c65f6" />

 
ls file1
## OUTPUT
<img width="487" height="427" alt="1yy" src="https://github.com/user-attachments/assets/4acc008b-a10d-451e-9d4f-992d0a282d4e" />

echo $?
## OUTPUT 
<img width="312" height="73" alt="1zz" src="https://github.com/user-attachments/assets/a814d735-1870-4183-aa75-41e9b1139f58" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="335" height="75" alt="aaa" src="https://github.com/user-attachments/assets/629fe4a3-ca6f-46ef-946d-ddb6ebb960c1" />

abcd
 
echo $?
 ## OUTPUT

<img width="322" height="72" alt="bbb" src="https://github.com/user-attachments/assets/c2fc8c3b-569d-472c-a204-1e901cf641e5" />

 
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

<img width="417" height="77" alt="ccc" src="https://github.com/user-attachments/assets/d66a7c2e-cb43-4f93-83b5-043f5e1e9790" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="365" height="275" alt="ddd" src="https://github.com/user-attachments/assets/d2094c07-6775-442c-bef7-e459506e838f" />


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
<img width="660" height="262" alt="fff" src="https://github.com/user-attachments/assets/22ddaeab-8b7a-4760-8e8d-ae41b151760b" />

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

<img width="501" height="382" alt="hhh" src="https://github.com/user-attachments/assets/729fb841-77f2-4f70-8073-fa11ee5d165e" />

<img width="593" height="147" alt="jjj" src="https://github.com/user-attachments/assets/88b3333e-7879-40e7-aee1-2814d44674d8" />

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
<img width="625" height="177" alt="lll" src="https://github.com/user-attachments/assets/687bedc2-62d0-4c05-ae92-48f27a77f1d7" />

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
<img width="643" height="152" alt="mmm" src="https://github.com/user-attachments/assets/40351ca0-677e-4035-ab34-834241dc4692" />

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
<img width="643" height="152" alt="mmm" src="https://github.com/user-attachments/assets/40d033a3-e649-45eb-902b-76f6e9bc18f7" />

<img width="621" height="132" alt="nnn" src="https://github.com/user-attachments/assets/18f26158-4f6d-4562-97fe-78e853cc70ce" />

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
<img width="556" height="107" alt="ooo" src="https://github.com/user-attachments/assets/a6130a86-d654-41e8-84aa-a7756450e502" />


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
<img width="475" height="293" alt="ppp" src="https://github.com/user-attachments/assets/b01f30c8-272e-4808-86c3-bea6e1dee750" />

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
<img width="352" height="118" alt="qqq" src="https://github.com/user-attachments/assets/7cbfd458-9e84-4b75-87d4-39c544d65759" />

 
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
 <img width="297" height="343" alt="rrr" src="https://github.com/user-attachments/assets/9f075817-a6bf-4624-b8cb-e2d03d50e5d4" />

 
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
 
 <img width="538" height="181" alt="sss" src="https://github.com/user-attachments/assets/b6416cfa-95df-4ca3-9503-0a6d4eafe68f" />

 
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
 
 <img width="363" height="217" alt="ttt" src="https://github.com/user-attachments/assets/e8979ef8-1c08-4f64-b09f-2e502696b5f5" />

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
 <img width="352" height="136" alt="uuu" src="https://github.com/user-attachments/assets/db76c90b-9b5b-48a1-8c5f-1771df3d2376" />

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
 <img width="621" height="291" alt="vvv" src="https://github.com/user-attachments/assets/a1d6cdd9-a28d-4132-bc34-6c26b6fa2478" />

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
<img width="415" height="387" alt="yyy" src="https://github.com/user-attachments/assets/a0c1c615-94b4-4f8f-8646-872cb58247ec" />

 
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
<img width="333" height="230" alt="zzz" src="https://github.com/user-attachments/assets/999c3a74-5780-4ec7-9d5f-df49cb3972c5" />

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
<img width="341" height="315" alt="aaaa" src="https://github.com/user-attachments/assets/997c9d52-731a-4b1b-bf02-ba510ea3304b" />

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
 
<img width="348" height="198" alt="bbbb" src="https://github.com/user-attachments/assets/3e01600a-54d1-4f3e-9001-356f786aef30" />


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
<img width="408" height="400" alt="dddd" src="https://github.com/user-attachments/assets/9ff0df8f-af31-4b46-a8da-f3998aada6ab" />

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
<img width="436" height="223" alt="eeee" src="https://github.com/user-attachments/assets/4fe6bebf-b004-443a-a3d7-456db4f9d797" />


# RESULT:
The Commands are executed successfully.
