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

<img width="420" height="121" alt="image" src="https://github.com/user-attachments/assets/c62032eb-8a73-4401-90dc-9439211804da" />


cat < file2
## OUTPUT
<img width="446" height="181" alt="image" src="https://github.com/user-attachments/assets/6f3b8852-3223-409b-8c94-d76bfd6a7774" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="491" height="50" alt="image" src="https://github.com/user-attachments/assets/d770c19e-d37d-4a64-9c23-3b6408dfdc3c" />

comm file1 file2
 ## OUTPUT
<img width="491" height="50" alt="image" src="https://github.com/user-attachments/assets/2ee6b59a-acc3-48ce-b74e-52ab003f0002" />

 
diff file1 file2
## OUTPUT
<img width="574" height="349" alt="image" src="https://github.com/user-attachments/assets/15267863-6bf9-4564-ac78-2230bcd44520" />


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

<img width="457" height="102" alt="image" src="https://github.com/user-attachments/assets/54688432-04c5-43fb-9396-7fdd473552ed" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="490" height="122" alt="image" src="https://github.com/user-attachments/assets/894cbc45-893f-47f6-9f34-ac120fbd7386" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="516" height="132" alt="image" src="https://github.com/user-attachments/assets/1c21b9ad-4031-4692-8f11-8d03da2eccff" />

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
<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/39a5ba36-95b8-4fd3-b454-8504a52b7c6f" />

grep hello newfile 
## OUTPUT

<img width="482" height="62" alt="image" src="https://github.com/user-attachments/assets/af2d168a-8ddc-47d2-ae7b-bde6aa08b4b9" />

grep -v hello newfile 
## OUTPUT
<img width="513" height="77" alt="image" src="https://github.com/user-attachments/assets/b980ca4c-69aa-446c-ae98-164788c70123" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="638" height="97" alt="image" src="https://github.com/user-attachments/assets/6af69a93-1315-4d61-b44d-65e7fd02b70c" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="692" height="69" alt="image" src="https://github.com/user-attachments/assets/d02443af-0ca0-4de7-b400-48519d74b431" />

grep -R ubuntu /etc
## OUTPUT

<img width="745" height="238" alt="image" src="https://github.com/user-attachments/assets/1b230e68-8401-4e57-ba32-e6ba6ffdbfef" />

grep -w -n world newfile   
## OUTPUT
<img width="726" height="96" alt="image" src="https://github.com/user-attachments/assets/aec08f29-ba7f-4d8c-9ae0-8040868313ae" />


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

<img width="717" height="99" alt="image" src="https://github.com/user-attachments/assets/8d7007df-4100-452e-8de3-12be911dd4b0" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="627" height="89" alt="image" src="https://github.com/user-attachments/assets/70b39fa6-8741-409f-9c0e-b5a674e62bc7" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="698" height="88" alt="image" src="https://github.com/user-attachments/assets/91038bfe-0b72-4eaf-bbda-b6dff122fd3d" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="550" height="69" alt="image" src="https://github.com/user-attachments/assets/eab059f0-1a0e-42c3-9368-43bd5f1c8a41" />

egrep '(world$)' newfile 
## OUTPUT


<img width="550" height="69" alt="image" src="https://github.com/user-attachments/assets/91e2746e-643a-4a64-ad02-52053c153dc5" />

egrep '(World$)' newfile 
## OUTPUT


<img width="608" height="66" alt="image" src="https://github.com/user-attachments/assets/238af6d5-08b8-4177-8331-1fd9db16c604" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="605" height="92" alt="image" src="https://github.com/user-attachments/assets/13499b61-4ca6-41a0-8afa-73fb19ee2945" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="592" height="68" alt="image" src="https://github.com/user-attachments/assets/5b9610ec-f9f3-48ce-8407-b0c726bd7958" />

egrep 'Linux.*world' newfile 
## OUTPUT



<img width="619" height="64" alt="image" src="https://github.com/user-attachments/assets/8590acb6-29f0-4642-ac3e-bc1a80054267" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="619" height="64" alt="image" src="https://github.com/user-attachments/assets/f738124f-bf09-41b3-81c2-9b276786e381" />

egrep l{2} newfile
## OUTPUT
<img width="727" height="98" alt="image" src="https://github.com/user-attachments/assets/2d76d920-8255-485a-9c47-02e9bc875b28" />

egrep 's{1,2}' newfile
## OUTPUT 



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


<img width="514" height="59" alt="image" src="https://github.com/user-attachments/assets/8c08932b-a396-403a-b791-c54a20b13f44" />


sed -n -e '$p' file23
## OUTPUT


<img width="536" height="64" alt="image" src="https://github.com/user-attachments/assets/846e1b9d-eff2-4f63-a753-a408df4e61a3" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="592" height="263" alt="image" src="https://github.com/user-attachments/assets/45085a9e-10aa-4c91-938d-d6373aed70a4" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="595" height="272" alt="image" src="https://github.com/user-attachments/assets/d4fe48bb-cce8-47ec-aed4-f43febd75cc5" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="648" height="278" alt="image" src="https://github.com/user-attachments/assets/d255ad9e-3123-4ea4-991f-4b84b7c240be" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="592" height="180" alt="image" src="https://github.com/user-attachments/assets/d5f9c51e-d15a-4a9a-b5c4-fd1715c685a8" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="581" height="119" alt="image" src="https://github.com/user-attachments/assets/4c15ac62-d523-4ac0-943a-76c5c19b804f" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="636" height="86" alt="image" src="https://github.com/user-attachments/assets/4e5b002b-90ff-444e-bc6d-28bd19eeb761" />

seq 10 
## OUTPUT

<img width="556" height="335" alt="image" src="https://github.com/user-attachments/assets/11784e21-ac42-4826-ac79-223bd178ce04" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="548" height="120" alt="image" src="https://github.com/user-attachments/assets/295d89ba-3216-48f1-9467-139291f05753" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="554" height="119" alt="image" src="https://github.com/user-attachments/assets/47bfb17b-8f5b-4b8f-946b-c33846bdffce" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="561" height="119" alt="image" src="https://github.com/user-attachments/assets/c3ab8941-48bf-4b96-b262-60d63fc4a956" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="562" height="144" alt="image" src="https://github.com/user-attachments/assets/48fec7c0-d6b9-4524-9bcc-86a5d9bf8272" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="570" height="119" alt="image" src="https://github.com/user-attachments/assets/778ed177-d9ff-4d4b-beea-c79d7faaaadf" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="573" height="104" alt="image" src="https://github.com/user-attachments/assets/525958d1-b12e-4429-8ec2-828e8dd9c1e0" />

sed -n '2,4{s/$/*/;p}' file23

<img width="609" height="122" alt="image" src="https://github.com/user-attachments/assets/0d1d2812-143d-4d90-84d6-df568ba5fcc0" />

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

<img width="406" height="189" alt="image" src="https://github.com/user-attachments/assets/dd600f27-a06f-437b-b842-5fd25279a292" />

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

<img width="380" height="175" alt="image" src="https://github.com/user-attachments/assets/bbe2ff38-4187-4775-8c7d-7204e43dc04f" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="634" height="114" alt="image" src="https://github.com/user-attachments/assets/a3f33b5c-eea4-435e-9a2b-0c700cfb0983" />

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

<img width="694" height="258" alt="image" src="https://github.com/user-attachments/assets/4f30566d-5629-4f72-9368-10f7d8a07a02" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="746" height="120" alt="image" src="https://github.com/user-attachments/assets/6b3af265-b4fc-447a-92fd-c4e7ee35d5a5" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="367" height="89" alt="image" src="https://github.com/user-attachments/assets/4aee93d7-91cd-4f6f-b298-cbf68620088e" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="288" height="86" alt="image" src="https://github.com/user-attachments/assets/f5f27573-ea30-45f5-87b8-06057622aac4" />

tar -xvf backup.tar
## OUTPUT

<img width="766" height="147" alt="image" src="https://github.com/user-attachments/assets/cc422a6c-8c5c-4c5a-a90e-31fcfef23296" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="764" height="156" alt="image" src="https://github.com/user-attachments/assets/81a3c2e5-adec-41f8-af1e-ac88d35489d6" />

gunzip backup.tar.gz
## OUTPUT

<img width="767" height="222" alt="image" src="https://github.com/user-attachments/assets/52de55f8-bd06-4a72-a5d0-940363f0b0f6" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="750" height="313" alt="image" src="https://github.com/user-attachments/assets/24457d4f-0c06-4ae6-a60b-fecd23738944" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="433" height="122" alt="image" src="https://github.com/user-attachments/assets/01ffdce4-f9a6-491c-8a7b-a92172d832d7" />

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

<img width="538" height="433" alt="image" src="https://github.com/user-attachments/assets/871e8495-1ec0-4416-b1b5-5478de5dff3a" />

ls file1
## OUTPUT

<img width="324" height="56" alt="image" src="https://github.com/user-attachments/assets/30d2c095-9106-4920-a3da-e382a4e99c32" />

echo $?
## OUTPUT 

<img width="314" height="65" alt="image" src="https://github.com/user-attachments/assets/e5e7f3be-41e5-45a3-a92d-8368a3bc7345" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="316" height="64" alt="image" src="https://github.com/user-attachments/assets/1f22b4cf-415e-47ef-b4c9-bd99b1f9f773" />

abcd
 
echo $?
 ## OUTPUT

<img width="652" height="299" alt="image" src="https://github.com/user-attachments/assets/20043573-d952-4710-ac52-2ee692af28f4" />
 
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

<img width="641" height="328" alt="image" src="https://github.com/user-attachments/assets/87f40207-c050-44c1-a777-e62e377a128f" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="781" height="316" alt="image" src="https://github.com/user-attachments/assets/8215c818-47fa-4c3f-9f56-7bdc1f856e6b" />

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

<img width="777" height="233" alt="image" src="https://github.com/user-attachments/assets/9a822fd5-960a-4734-801f-2f57c5cbc0ba" />

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

<img width="685" height="543" alt="image" src="https://github.com/user-attachments/assets/06ca8435-8485-4c36-9e51-fc5a70bbec12" />

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

<img width="729" height="648" alt="image" src="https://github.com/user-attachments/assets/88b4e735-3cba-4c7d-8159-e089b99276d8" />

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


<img width="759" height="653" alt="image" src="https://github.com/user-attachments/assets/a697e7f2-bb5d-4651-9909-b6f177a2f7af" />

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

<img width="755" height="636" alt="image" src="https://github.com/user-attachments/assets/de2dff0e-be3f-4d70-b5c0-7de3de429195" />


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

<img width="682" height="341" alt="image" src="https://github.com/user-attachments/assets/bcc8da70-6e59-46f3-b659-9f81a065fd81" />

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

<img width="525" height="267" alt="image" src="https://github.com/user-attachments/assets/5a0f70e0-7b2b-4ac4-9160-fb790fb7f092" />

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

<img width="513" height="275" alt="image" src="https://github.com/user-attachments/assets/0c646439-2de2-40a8-b410-a58c80fab844" />


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

<img width="775" height="290" alt="image" src="https://github.com/user-attachments/assets/f0986e03-65d6-45d2-a3c3-136e59dbd6a4" />

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

<img width="513" height="275" alt="image" src="https://github.com/user-attachments/assets/c1eec4d4-1115-49f7-9b3e-3231e825f433" />

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

<img width="769" height="286" alt="image" src="https://github.com/user-attachments/assets/6b84491b-ab8c-43fe-88bc-53af7c7c6ab3" />

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

<img width="775" height="290" alt="image" src="https://github.com/user-attachments/assets/f1bbc16c-1031-42c0-bdf6-1e5e987ebcd2" />

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

<img width="586" height="183" alt="image" src="https://github.com/user-attachments/assets/1984c1ff-ddfe-4daa-90a1-b864e9a70d57" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="642" height="142" alt="image" src="https://github.com/user-attachments/assets/8e4761c8-4ea6-4b67-ab25-b962c08d109f" />

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

<img width="457" height="22" alt="image" src="https://github.com/user-attachments/assets/e33d5279-abcc-4992-9eed-4237fa0f2b3c" />

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

<img width="191" height="69" alt="image" src="https://github.com/user-attachments/assets/ea89540b-dd52-4e5c-889b-32bbf3236efb" />

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

<img width="191" height="69" alt="image" src="https://github.com/user-attachments/assets/ecbd9cf1-57e9-46ee-b1c7-80f28bf6f3f6" />

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

<img width="660" height="369" alt="image" src="https://github.com/user-attachments/assets/c8cfb8d0-931b-44a2-a4c4-9583c394e4c0" />

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

<img width="457" height="245" alt="image" src="https://github.com/user-attachments/assets/dd7f9c1c-4621-414d-8cb6-7d9996bbc035" />

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

<img width="682" height="371" alt="image" src="https://github.com/user-attachments/assets/677dff1b-15cf-4b2d-8498-84156c6025d9" />

# RESULT:
The Commands are executed successfully.
