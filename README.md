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


![image](https://github.com/user-attachments/assets/feb18b6c-07ac-47fd-9864-b217a0855334)


cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/3d96ae49-881f-44ca-ac64-7c39b49a271d)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/ade5598c-97eb-48fa-876a-c03f3a93b38e)



comm file1 file2
 ## OUTPUT


![image](https://github.com/user-attachments/assets/74b1bbf6-1e35-48ae-b1d6-a8834a256565)

 
diff file1 file2
## OUTPUT


![image](https://github.com/user-attachments/assets/fdb78f6c-8d5f-4776-b9dd-6cb7d5abca69)


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

![image](https://github.com/user-attachments/assets/81776079-1539-4971-bbe2-edc1972b897e)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/a0e18500-1407-4047-995f-196ad49311c2)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/0bcfd63b-3932-485d-bf88-a3be0cf19385)



cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 

![image](https://github.com/user-attachments/assets/5ded0f08-1b22-40dc-a557-f84d35e2230a)

 
grep Hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/821b94dd-dfe8-40f9-8f73-1330534d5fd6)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0b5cea68-4f62-4fa4-abee-7123a316efa1)



grep -v hello newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/384b0dad-6c38-4d67-bd37-a274fe6cca94)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/e7f971ec-be2e-4301-abb9-307da2eec3bf)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/3979be2c-f818-400f-b264-24623310712a)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/f0084d5a-f2bd-4335-bff5-48f98158d49d)


grep -w -n world newfile   
## OUTPUT

![image](https://github.com/user-attachments/assets/4f3d83a3-d785-4643-b570-05c9588307ae)



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

![image](https://github.com/user-attachments/assets/814ad67b-5265-4dad-a5bf-7d28babed846)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d7887fda-0dd9-4cbb-9d7f-56328cfdd885)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/2154a939-8eda-401b-9d7b-27028058cea3)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f2a10174-171d-4a1f-b00a-3fd436730655)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/be5c065b-088f-44dd-9203-d0c0d82594b3)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/205b2246-3fd3-4aa2-a51f-fb52d1a8e48f)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/edf8a23b-fe0f-49b2-9abb-5a45e0f0eed7)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/3f773deb-0088-4b16-8b4e-6fa3b66702e6)


egrep 'Linux.*world' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/7a1ebdd3-f7df-499d-a643-bbe213012247)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/a01caf8c-b108-4a07-ade8-ddc65e6339f6)



egrep l{2} newfile
## OUTPUT


![image](https://github.com/user-attachments/assets/75ae0bfb-526b-405b-88ba-719a5824caa4)



egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/7a6f45f3-8e28-4752-a212-4c97e385374f)



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

![image](https://github.com/user-attachments/assets/0aba266e-92b6-4c8a-a4a4-8287193fcf78)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/816b90d8-6744-4e67-a76b-94aa0aca3df5)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/8f177a1d-009e-4cd3-91ae-1c7f66a4dad9)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/0ac6296c-8cce-47ff-84fb-1abba218b4f0)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/51d88b01-ada0-4702-861a-521f19e267c0)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/e17e5fc3-9418-4c04-8f60-8347efb2dd40)



sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/0fe5374c-e8a3-4f02-a870-8c766870937e)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/14440b63-9afe-47b3-843c-f559062b5a92)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/9b8a0b9b-b58e-4144-b4d9-2b1a4bc208a6)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/d098a824-a538-4b6d-a488-d1d6a5ecf040)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/be1b3ca6-ab8b-4124-8fd3-2739fe5feb77)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/c6bd117b-0ce5-4f6c-bc93-29f6f0243d97)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/a540559c-4c6b-4fe2-b0c9-241b55dfbdc7)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/24e138ab-6958-490e-96b6-534231ec3cf0)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/3fde20c8-612f-478b-a0d6-9eaabd17f4ea)


sed -n '2,4{s/$/*/;p}' file23

![image](https://github.com/user-attachments/assets/d5e09363-7c50-47eb-9940-570f4475f432)

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
![image](https://github.com/user-attachments/assets/5a14c59c-56e4-42be-9834-05c68d3296cb)


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

![image](https://github.com/user-attachments/assets/0b8521ee-67b6-4768-b3bd-ef0ae49bc29c)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/fa3c54b8-4e5c-40ac-9d55-8f49f710563a)

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

![image](https://github.com/user-attachments/assets/6325c0ab-1d7b-4d01-9ab8-9f9f589488ef)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/5a42af66-6227-4afe-985c-ce29dec848f4)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/2c4af4cf-07f3-4dcf-a7b8-71f13422546c)
![image](https://github.com/user-attachments/assets/d289e39b-b209-4153-842c-dc02e1827ee3)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/059ad85d-b25d-4213-a9eb-9c1cbd7c8876)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/cbc10542-d5bd-4211-acf7-84d9fb174773)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/79dcb4cf-7fc0-4b3a-8909-b04035450ed0)

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

 ![image](https://github.com/user-attachments/assets/553313d2-23b3-494f-9945-0a5106533b19)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/2d7237f3-e68c-4030-8aa1-385fde64b5f9)


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

![image](https://github.com/user-attachments/assets/5ae29e32-6e77-48e2-aec2-12cff03368ac)
 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/9f9ca5e2-cc93-43c2-8b9a-47f1631d84c7)


echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/d3223ddf-20e8-4620-bd3b-2c8779de9c19)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/18492649-ba1d-4ba5-9ad4-08f73b89efab)

 
abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/145cc610-eea7-4aa2-b2c2-c34683fc3121)

 
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

![image](https://github.com/user-attachments/assets/a699281e-c93d-499c-b661-73962c8cfdbe)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/40a0bd54-80d0-4c4a-890f-81c0c7578fc0)


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
