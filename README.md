<img width="1257" height="800" alt="image" src="https://github.com/user-attachments/assets/f84d4867-56d1-4286-b359-7b9dc8715338" /># OS-Linux-commands-Shell-scripting
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

<img width="766" height="787" alt="image" src="https://github.com/user-attachments/assets/21a84db3-62f5-470e-9c82-b36a2010967e" />

cat < file2
## OUTPUT

<img width="1077" height="207" alt="image" src="https://github.com/user-attachments/assets/8ccdc47c-68e4-4ea5-b205-382920f067f5" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="727" height="87" alt="image" src="https://github.com/user-attachments/assets/f0f48965-6341-43b4-ac49-21a0659f3e9a" />

 
comm file1 file2
 ## OUTPUT
 
<img width="1182" height="275" alt="image" src="https://github.com/user-attachments/assets/9988ae52-52fd-4696-92a0-0ee99a822d1f" />

diff file1 file2
## OUTPUT

<img width="977" height="336" alt="image" src="https://github.com/user-attachments/assets/442e4b33-293b-4bf6-a5ea-f83ad3cf6d43" />


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

<img width="1156" height="367" alt="image" src="https://github.com/user-attachments/assets/ee6f6299-3178-4c1e-86c0-c55502bea8ed" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="921" height="202" alt="image" src="https://github.com/user-attachments/assets/da354d28-8378-41d4-bc46-e0ffb42becf0" />

cut -d "|" -f 2 file22
## OUTPUT

<img width="865" height="152" alt="image" src="https://github.com/user-attachments/assets/68e1c7f3-8746-49f2-ae64-055a26e265e7" />


cat > newfile 
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

<img width="1227" height="202" alt="image" src="https://github.com/user-attachments/assets/3aaf5bf0-e0a6-446f-9564-e819a0957814" />

grep hello newfile 
## OUTPUT

<img width="865" height="87" alt="image" src="https://github.com/user-attachments/assets/31f9ae77-8d94-4bb8-988e-61dc082ebf33" />

grep -v hello newfile 
## OUTPUT

<img width="957" height="86" alt="image" src="https://github.com/user-attachments/assets/89978a2f-456d-488f-a5fa-734a9b8dfaab" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="935" height="115" alt="image" src="https://github.com/user-attachments/assets/c8e3d371-3670-4793-810c-c671fbdb5ba6" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1022" height="87" alt="image" src="https://github.com/user-attachments/assets/00e3b88c-438c-42fc-8834-61ee2e3382b4" />


grep -R ubuntu /etc
## OUTPUT

<img width="1917" height="862" alt="image" src="https://github.com/user-attachments/assets/c4cae2b0-9ebd-45bb-9201-93a6edc0b162" />


grep -w -n world newfile   
## OUTPUT

<img width="1167" height="106" alt="image" src="https://github.com/user-attachments/assets/29e5a649-1c0b-41f4-88ea-92b7e5c13036" />


cat > newfile 
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

<img width="1436" height="520" alt="image" src="https://github.com/user-attachments/assets/65044ea7-4f56-48ba-bb58-bbcc29307459" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="915" height="117" alt="image" src="https://github.com/user-attachments/assets/d68d963c-c19d-40e6-a972-e47d18f768fb" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1050" height="117" alt="image" src="https://github.com/user-attachments/assets/6d7faafb-2103-422d-92b1-6d1bdd3296e4" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="1110" height="90" alt="image" src="https://github.com/user-attachments/assets/14bd63ac-2715-4b29-a394-22c5dba2c6a5" />

egrep '(world$)' newfile 
## OUTPUT

<img width="1171" height="112" alt="image" src="https://github.com/user-attachments/assets/1b379f3a-b091-40d0-9285-57ba2e1ef789" />


egrep '(World$)' newfile 
## OUTPUT

<img width="992" height="90" alt="image" src="https://github.com/user-attachments/assets/26e5e5e7-bdfc-493f-8f36-27233873b598" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1107" height="166" alt="image" src="https://github.com/user-attachments/assets/99b9100c-bda0-4f19-b5d7-46f3ae202084" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1170" height="105" alt="image" src="https://github.com/user-attachments/assets/f892bbe6-a0c9-44cd-bb51-4d59f2474c4a" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="965" height="105" alt="image" src="https://github.com/user-attachments/assets/faa2634e-7610-446d-b41a-c9128142b479" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1007" height="100" alt="image" src="https://github.com/user-attachments/assets/407595b9-3831-42e4-9c4d-a4eed35dd594" />


egrep l{2} newfile
## OUTPUT

<img width="856" height="122" alt="image" src="https://github.com/user-attachments/assets/dbc23d8f-038f-41a1-a375-c6a97f5ee827" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1052" height="162" alt="image" src="https://github.com/user-attachments/assets/c05946a0-7093-4e04-b1b9-ef0d112aaa15" />


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

```


sed -n -e '3p' file23
## OUTPUT

<img width="920" height="382" alt="image" src="https://github.com/user-attachments/assets/7ba93cea-5328-42e4-bfaf-29aa769e34a6" />


sed -n -e '$p' file23
## OUTPUT

<img width="1152" height="97" alt="image" src="https://github.com/user-attachments/assets/2683ab8d-5234-41dd-82d8-6dd0d3e0bda7" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1052" height="300" alt="image" src="https://github.com/user-attachments/assets/8255a90d-d285-44fd-829f-cbe97958294b" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1015" height="307" alt="image" src="https://github.com/user-attachments/assets/aa72b579-53d9-49d2-ab54-9c5a42e7fac3" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="887" height="310" alt="image" src="https://github.com/user-attachments/assets/0b31c27f-2899-4f23-ade4-33a5e3b0d2ce" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1075" height="222" alt="image" src="https://github.com/user-attachments/assets/57992eaa-d98d-45e1-9bc8-31e252a8eb52" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="982" height="166" alt="image" src="https://github.com/user-attachments/assets/2c36e05f-c505-4d79-84f0-b1cc0da0afd2" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1250" height="107" alt="image" src="https://github.com/user-attachments/assets/ae4c3da9-b7f1-434c-b09e-1fff49bf0dec" />

seq 10 
## OUTPUT

<img width="786" height="372" alt="image" src="https://github.com/user-attachments/assets/5fa737f0-85d5-4cb6-9a4d-6a4dbcd8e1af" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="605" height="157" alt="image" src="https://github.com/user-attachments/assets/d639da96-6164-482b-9369-e118efa9149d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="765" height="162" alt="image" src="https://github.com/user-attachments/assets/308d7778-b9ec-4d9e-bb14-f5ae999d5844" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="775" height="182" alt="image" src="https://github.com/user-attachments/assets/61400a3d-fade-4c53-b0bf-530bfda0a3e0" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="715" height="145" alt="image" src="https://github.com/user-attachments/assets/c9c8a81c-2fce-4413-9ef0-95f4d284b3e9" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="785" height="150" alt="image" src="https://github.com/user-attachments/assets/48582dc0-1ce3-449b-9c9c-477d56691169" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1025" height="157" alt="image" src="https://github.com/user-attachments/assets/3ca4822a-9487-4829-a60b-d09f00e03c73" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="690" height="157" alt="image" src="https://github.com/user-attachments/assets/5528684a-1209-49f9-b6e6-db3de1a3f7e0" />


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

<img width="1015" height="427" alt="image" src="https://github.com/user-attachments/assets/6147cd9e-9d92-426b-9ba7-621e06779698" />


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

<img width="1045" height="451" alt="image" src="https://github.com/user-attachments/assets/33be5798-c9d7-4279-b8b0-e9be17cbc349" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="801" height="302" alt="image" src="https://github.com/user-attachments/assets/21ad5fa9-d737-4a61-9a2d-6be9d3e8174d" />


cat > urllist.txt
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

<img width="811" height="302" alt="image" src="https://github.com/user-attachments/assets/83142fca-46cd-43e5-8250-ea03699c1d76" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="785" height="152" alt="image" src="https://github.com/user-attachments/assets/bcaa0563-04f0-498b-94c8-2b9ca31fe738" />

## Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="715" height="302" alt="image" src="https://github.com/user-attachments/assets/c8dcd4c8-83aa-4607-938c-02f64997aef7" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1211" height="347" alt="image" src="https://github.com/user-attachments/assets/19fd3d65-c8ab-472a-8e5b-1423e38ba629" />


tar -xvf backup.tar
## OUTPUT

<img width="925" height="195" alt="image" src="https://github.com/user-attachments/assets/845267c6-ecc2-4aa3-a32d-82b04f9c0a59" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="1085" height="155" alt="image" src="https://github.com/user-attachments/assets/14e49917-f23e-43eb-89e3-e5e0cb6512ba" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="1157" height="142" alt="image" src="https://github.com/user-attachments/assets/aecca3a8-2f6a-4210-83d0-6ae31a9f1dcc" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="1282" height="257" alt="image" src="https://github.com/user-attachments/assets/23ed0c41-266e-4c54-ad96-219580a63b5e" />

 
cat << stop > herecheck.txt

```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1105" height="330" alt="image" src="https://github.com/user-attachments/assets/6862a3e6-886f-48c0-9324-5647e03d1c9d" />


cat > scriptest.sh 
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

<img width="1151" height="767" alt="image" src="https://github.com/user-attachments/assets/0a0c3237-23d9-4c78-a04f-09245e6931e5" />
<img width="956" height="717" alt="image" src="https://github.com/user-attachments/assets/e3a891bf-849b-4d3f-b2ff-a3f688fe9631" />

 
ls file1
## OUTPUT

<img width="960" height="100" alt="image" src="https://github.com/user-attachments/assets/f0a94001-0795-4439-8d93-0e8d43be678b" />


echo $?
## OUTPUT 

<img width="970" height="92" alt="image" src="https://github.com/user-attachments/assets/f8f5c842-c4e7-4b69-9786-771840c59253" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="940" height="177" alt="image" src="https://github.com/user-attachments/assets/7288df3b-e936-4b5c-a975-db68c1753545" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="1052" height="272" alt="image" src="https://github.com/user-attachments/assets/52822ddd-6b18-42eb-b4b4-0110664bd6c2" />

 
# mis-using string comparisons

cat > strcomp.sh 
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


<img width="1007" height="712" alt="image" src="https://github.com/user-attachments/assets/4a11d525-d0b7-4dc1-a3ff-0d9eeb84421c" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="1220" height="152" alt="image" src="https://github.com/user-attachments/assets/966974cc-60b7-44d3-974a-762aa04d1088" />


# check file ownership
cat > psswdperm.sh 
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

<img width="906" height="620" alt="image" src="https://github.com/user-attachments/assets/69da02d6-f3d2-403b-990b-d1e1187e93c7" />

<img width="866" height="151" alt="image" src="https://github.com/user-attachments/assets/b18b4793-ed50-486e-b257-ec3bde1f6d7a" />

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

<img width="1257" height="800" alt="image" src="https://github.com/user-attachments/assets/5fd3899d-77ae-471a-8d05-d13eebf5ede0" />

<img width="1276" height="682" alt="image" src="https://github.com/user-attachments/assets/6a2c9ce9-4f19-4216-85a1-1bc976c44bc0" />


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

<img width="1335" height="656" alt="image" src="https://github.com/user-attachments/assets/f2b6498f-6847-4dbe-862f-6c6fed8a69f3" />


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

<img width="970" height="380" alt="image" src="https://github.com/user-attachments/assets/90bf43e4-c762-47c0-9cf0-bf051de91467" />


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

## output:

<img width="886" height="602" alt="image" src="https://github.com/user-attachments/assets/a2a45579-ec80-44db-a875-67449c8a9061" />

 
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

<img width="792" height="601" alt="image" src="https://github.com/user-attachments/assets/30da6337-0386-44ca-bc2d-a47aceba6dae" />



$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 <img width="772" height="361" alt="image" src="https://github.com/user-attachments/assets/57f77e00-bb11-442e-aee4-a3046e91c982" />


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
 
## output:

<img width="840" height="727" alt="image" src="https://github.com/user-attachments/assets/7adb5254-e2dc-480b-bb3c-fd9ed7dcb32b" />

 
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

 <img width="932" height="587" alt="image" src="https://github.com/user-attachments/assets/8ff744a3-4fe5-43b9-b1a0-957a58654e5d" />

<img width="635" height="384" alt="image" src="https://github.com/user-attachments/assets/60d3b231-ebea-4d1b-8ef5-25b962799a1d" />

 
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

## output:

<img width="707" height="627" alt="image" src="https://github.com/user-attachments/assets/4f5af5ec-6705-431a-904f-1e89b45cd8c3" />

 
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
## output :

<img width="675" height="701" alt="image" src="https://github.com/user-attachments/assets/abdb25ea-1fdc-43bb-bba4-7b12204d86ed" />

 
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

<img width="675" height="675" alt="image" src="https://github.com/user-attachments/assets/c32d7638-9566-408e-88a2-750d94dc5f74" />


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

<img width="677" height="716" alt="image" src="https://github.com/user-attachments/assets/e4783ee0-50b6-4382-99f3-c1d82d125db2" />


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

<img width="691" height="676" alt="image" src="https://github.com/user-attachments/assets/ad1d37f8-9cdc-4ff4-8296-1f8da33289f7" />


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

<img width="676" height="542" alt="image" src="https://github.com/user-attachments/assets/5f371569-d395-48ee-9425-fffb4170d49e" />


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
 
<img width="685" height="707" alt="image" src="https://github.com/user-attachments/assets/5a042632-0cf4-4a95-bafc-9d02f44c17db" />

<img width="698" height="730" alt="image" src="https://github.com/user-attachments/assets/906f588f-e529-4419-b19b-8564947affc8" />

 
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
