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
![432225731-1bb3120c-1238-4920-a7ea-2ec3150d32b4](https://github.com/user-attachments/assets/4c7987ad-876c-4f06-8630-4c334c54af66)



cat < file2
## OUTPUT
![432226609-af32b9fb-66a8-4474-b17b-d75b9b7926d4](https://github.com/user-attachments/assets/20c5b426-62b0-404f-9ccc-ac585e079e53)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![432231466-fe022908-c0d6-4750-a3af-08e4f0928dcb](https://github.com/user-attachments/assets/72f1bb87-89b6-4d84-8dc8-b379fddaaece)

comm file1 file2
 ## OUTPUT
![432231816-4e232ce9-64ca-4bde-9d12-5f98108d8346](https://github.com/user-attachments/assets/9d93aa8e-3898-4af2-80e1-1eb5fa9940af)

 
diff file1 file2
## OUTPUT
![432232583-16204101-b55b-4a1c-835f-9bb417dfac40](https://github.com/user-attachments/assets/f65af3c6-93a5-4866-a3a4-6f288d5202d8)


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
![432234070-00c489fe-0939-43f2-b5cf-f571c047250d](https://github.com/user-attachments/assets/e9c3c0f5-f8ca-4d2a-bb69-427603173cf3)




cut -d "|" -f 1 file22
## OUTPUT

![432235004-eef254a6-6aa9-4363-986d-af6a4e32503b](https://github.com/user-attachments/assets/df92b85d-60de-43a6-acdf-7dd483145eb6)


cut -d "|" -f 2 file22
## OUTPUT
![432235451-b78a2f7e-6686-4576-a855-78896122233d](https://github.com/user-attachments/assets/565f273f-aa3c-4fdd-9243-f16dc50e5361)


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
![432236299-2572e17d-61ce-47f1-b253-d351109263a8](https://github.com/user-attachments/assets/3d17cd1f-7c8a-4cad-ade7-5309ee416235)



grep hello newfile 
## OUTPUT

![432236570-1ee46c9f-b7df-4ecf-913c-0aea790402f6](https://github.com/user-attachments/assets/18c0469d-6419-40f9-990d-4d0c0daf51db)



grep -v hello newfile 
## OUTPUT

![432237107-6a8b672b-5c17-41d6-840d-ad8af4cb25e7](https://github.com/user-attachments/assets/57414b43-caa3-4a2b-bd37-f1af41382d6b)


cat newfile | grep -i "hello"
## OUTPUT

![432237461-d7ff3b27-3730-4c8e-b763-fed7469c7cc2](https://github.com/user-attachments/assets/7ff1b466-58f9-4382-a6db-b3d871470716)



cat newfile | grep -i -c "hello"
## OUTPUT


![432237716-31eda373-42d7-403e-93b8-3942a6f8823a](https://github.com/user-attachments/assets/a49fae54-5681-41af-aceb-68b86ac39094)


grep -R ubuntu /etc
## OUTPUT
![432238537-8dde9438-13f6-4e9c-9ab6-1cd908c51940](https://github.com/user-attachments/assets/c918d963-4663-4958-b38e-1ab344ee525f)



grep -w -n world newfile   
## OUTPUT
![432239195-9c65ea2b-f5ad-4a02-88fd-03ed6741c893](https://github.com/user-attachments/assets/3f6ada39-cfb0-441b-831d-de045d26a0eb)


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
![432240596-c39fda35-314c-4fd4-a263-9803cc1aaaf3](https://github.com/user-attachments/assets/6009ca13-d94e-4299-a780-7ace2a7559f9)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![432240869-eed0c643-a36c-44ea-a416-38dcf24bfd94](https://github.com/user-attachments/assets/c330c7e7-6d07-4b7e-9eb1-b0bd2c081c65)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![432241187-2407a2da-bc0d-4dd0-8551-76e5a0ea5e05](https://github.com/user-attachments/assets/e5345d21-ba1a-4c57-a176-45eeb1debb23)



egrep '(^hello)' newfile 
## OUTPUT

![432241461-44050480-107a-4e3f-8ade-bc1ac9627d95](https://github.com/user-attachments/assets/169dd4d7-ef48-451d-8c41-f13b5dd877a2)


egrep '(world$)' newfile 
## OUTPUT

![432241702-93889252-1369-46d2-b8d9-e0e3fd509f7b](https://github.com/user-attachments/assets/6123fbf8-ff5c-4f17-b4ad-be5bf1f338e0)


egrep '(World$)' newfile 
## OUTPUT

![432241773-f7e818eb-8ce4-4f31-af9e-3749c6a32b5e](https://github.com/user-attachments/assets/d4e25fb0-56f9-44d5-a569-3dda3bcff3c5)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![432242580-ad4c2dde-1e04-4590-8929-0b97142b2864](https://github.com/user-attachments/assets/911735f7-41b9-4f56-8200-b4d20aca08d8)



egrep '[1-9]' newfile 
## OUTPUT

![432242780-de1e8d0a-93fd-4d58-9be3-12cc208f55b8](https://github.com/user-attachments/assets/6672b03a-3910-4107-8e81-14bea51dd941)


egrep 'Linux.*world' newfile 
## OUTPUT

![432243204-7a6fdf4f-3c6b-4b40-b396-42e1802f79dc](https://github.com/user-attachments/assets/265b362e-ab3e-49fa-8173-7fd0a74f94c7)

egrep 'Linux.*World' newfile 
## OUTPUT
![432243473-8bd1e9ba-19d7-4fff-9ad9-e2bd30746e97](https://github.com/user-attachments/assets/994b77ed-64dc-4b2f-95a1-3089940d5f9d)


egrep l{2} newfile
## OUTPUT
![432243676-40fa2653-6700-4f6a-8f8b-719e562b415f](https://github.com/user-attachments/assets/9a2e92b8-12c7-452b-8056-2777ccad833d)



egrep 's{1,2}' newfile
## OUTPUT 
![432243972-1d2b3a5e-6409-474f-8be0-b21192414c1f](https://github.com/user-attachments/assets/3c45035f-8217-4172-9593-15fdb3f67a55)


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
![432245212-14ceb3c8-6905-4c47-a233-72552615d761](https://github.com/user-attachments/assets/1ec8015d-6323-4352-bf7c-158be5351d41)



sed -n -e '$p' file23
## OUTPUT
![432245626-7084c57b-3cbc-4397-a455-4962d6372bfe](https://github.com/user-attachments/assets/f857830a-7dc3-4483-8b22-b295730d7722)



sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![432246721-cce0ae77-a28f-4322-b316-c54d3eeea180](https://github.com/user-attachments/assets/2d6252b6-c96f-4963-ad35-249705739abb)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![432246962-2598f70d-bee9-4e49-8bdc-e97761ce74a5](https://github.com/user-attachments/assets/45d6f181-d7fb-4274-a92f-b10f534d6446)



sed -n -e '1,5p' file23
## OUTPUT

![432247424-d70d7409-ec60-4000-ac14-8c6079528a09](https://github.com/user-attachments/assets/e9575664-b903-4ebf-b1fe-231df86c5604)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![432247795-0ed148ba-7d73-46fc-ad9a-c2d87300c415](https://github.com/user-attachments/assets/60ba0642-f4a4-4b13-9076-4b9721f2c910)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![432248018-5432ce87-44fd-42cc-9e5d-7cdfc31739b2](https://github.com/user-attachments/assets/3b6fa513-0ca5-4505-81a9-20319545a7c1)

seq 10 
## OUTPUT
![432248797-fea8e390-8ae0-4a90-a28e-8d2b2c2c4c76](https://github.com/user-attachments/assets/8e821981-6db1-4e36-9364-f48967b21b55)



seq 10 | sed -n '4,6p'
## OUTPUT
![432249057-5fae905a-ba24-4765-8c93-def41c9264b4](https://github.com/user-attachments/assets/683eb3b9-2e4f-41c7-8441-4c12bde37e68)



seq 10 | sed -n '2,~4p'
## OUTPUT

![432249287-44312c45-a1f5-4c19-a82c-79e3f0d6d171](https://github.com/user-attachments/assets/d94d4cf9-4a00-4970-8806-0fa85012ba60)


seq 3 | sed '2a hello'
## OUTPUT
![432249640-76cd1775-4b5d-485c-a622-3de51dad01b4](https://github.com/user-attachments/assets/d56107f5-8648-45b3-8f58-b7f2fdf9a7fd)



seq 2 | sed '2i hello'
## OUTPUT
![432249866-9c38dd7b-fef7-4d2e-8791-caef77ced470](https://github.com/user-attachments/assets/2eee118f-3211-49b8-88f8-10fc817f9f95)


seq 10 | sed '2,9c hello'
## OUTPUT

![432250148-39431da3-26f8-47ee-98eb-1e818f80398e](https://github.com/user-attachments/assets/4728609d-965c-4346-b9f9-ea36a5f2d3c0)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![432250572-28da254d-8c2f-4fb9-bb7c-e678a52d4b8f](https://github.com/user-attachments/assets/ed04ff48-3ac8-4b85-b805-12165d6d9e81)


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
![432252380-5db50e6c-391d-4ba8-a38f-93846e4eba4c](https://github.com/user-attachments/assets/3d5e8549-844a-4043-9aad-5efb9954696e)


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
![432252817-de81f100-b407-4b5d-a3c4-e564b3d9b3b2](https://github.com/user-attachments/assets/301da8d1-b67c-451d-a179-5836a9ee8cea)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![432253098-8ba44fdd-6db2-4a8a-8768-397d16d1fb43](https://github.com/user-attachments/assets/e3b0b312-58bb-49c9-a553-24ec89319ed0)

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
![432253858-b0f4cf88-27be-4ead-80f7-08225513dd8a](https://github.com/user-attachments/assets/c6051ee7-f085-4493-a2b0-16544e079ae8)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![432254220-9b25a0f1-e752-4909-8598-82e5eb880ad4](https://github.com/user-attachments/assets/e9cec517-e422-4dee-b0e6-821602ae35d6)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![432254507-7f0aa5d5-785d-4c8e-949c-d1d879c66bef](https://github.com/user-attachments/assets/0d9f328d-5d69-4d37-94d8-d615235f8531)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![432606968-8c56c8fb-bd94-4513-8599-0566c847d152](https://github.com/user-attachments/assets/06f43959-fc38-4aae-a16f-ed28a4457d66)


tar -xvf backup.tar
## OUTPUT
![432607140-92c2b763-f1b8-4ded-90f3-0c1e51d63527](https://github.com/user-attachments/assets/bed96d28-81a4-4a65-ae47-e5bec3189e20)

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
![432608433-0932e73f-7810-4c97-bd78-241311cf159f](https://github.com/user-attachments/assets/a6023a7b-d44d-4fdb-9596-f9bd6597283a)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![432608735-7f41c8dc-54c2-46c4-8da7-c5ab566be484](https://github.com/user-attachments/assets/9d7e32e1-df8b-4ccb-9250-a687d556ebf6)


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
![432609654-e937d554-8cd1-4050-a573-3eeff4519d77](https://github.com/user-attachments/assets/61389fef-e78b-40c3-9fca-6dc210b857be)

 
ls file1
## OUTPUT
![432609787-2d3b80e3-d9a2-426f-a255-2fcf8b44b9c1](https://github.com/user-attachments/assets/8b3b38fe-4f2f-41a7-b493-4e1a0f67878d)

echo $?
## OUTPUT 
![432609898-80397abf-0009-41c7-9d67-c84ec7bae2ae](https://github.com/user-attachments/assets/e3eff0e8-437a-4ea4-8cad-c79a2a22c8cf)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

![432609988-e33fdeb7-12a1-46c6-b04a-c008a5119e00](https://github.com/user-attachments/assets/84e1eb64-70d5-4be0-bf73-66870d99159d)

 
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
![432610794-87d0f7ad-127f-481a-a2c6-95972550bfef](https://github.com/user-attachments/assets/900f3d52-d17e-4f26-9199-995de7ef3db4)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![432611344-81fd545e-7fcf-42a1-bf9e-6985a6a971d2](https://github.com/user-attachments/assets/e969c88b-8d5e-4f49-8cc7-7a068e1ecc3e)


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
![432612248-91a5283a-ca9d-4bea-8e7e-608d90716214](https://github.com/user-attachments/assets/463639dd-ef73-4012-902f-96b914b06d29)

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
![432612760-bcdae15b-82d6-4040-8e87-289b1139f3c6](https://github.com/user-attachments/assets/bae65cd9-d38d-4fe1-97fe-73aee96673ab)



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
![432613192-a17bf600-aa8f-48eb-8e2c-01b27a7a2599](https://github.com/user-attachments/assets/df88bc77-26fd-4cf0-bd1a-c91c70647cb4)

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
 ![432613981-3bcbb9f8-ca91-41f3-9c29-f7a9986f88e0](https://github.com/user-attachments/assets/1045711e-6b3f-4523-9c76-f26e04f64666)

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
![432614423-cddfced1-6aa4-4b6b-82c7-3ebd5633bee1](https://github.com/user-attachments/assets/365f07c3-caed-40ed-b151-c85f96f55702)


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
![432614701-8f2eca5f-682c-42cd-bae5-b8bef51dfdb4](https://github.com/user-attachments/assets/1539cf3c-0d84-4dcb-b1d3-c143059b17e0)

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
![432615797-e944ec20-f4d7-47df-a71b-9f5b69784b13](https://github.com/user-attachments/assets/733df103-5ebd-4d25-9dec-e0cb4e1d7b5d)

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
![432615962-c1e21c04-c88e-4989-86d5-635b2be6deef](https://github.com/user-attachments/assets/eedf45ed-1e98-406b-b864-effc07280400)


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
![432616282-cd8918fe-35f7-49e0-beb8-5b54a2b9682d](https://github.com/user-attachments/assets/7e5243e3-32a1-4c6c-a204-e26ba1a757a1)

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
![432617641-fa1001aa-71d9-4f42-b2c2-3c3c07094b0a](https://github.com/user-attachments/assets/ef56e83b-03ed-4611-a465-66a0e2081a04)

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
![432617921-783c7ff7-c516-4b2f-bcd6-1f6fa1679cca](https://github.com/user-attachments/assets/770056b3-8745-49ef-ae80-32fd4d32ff60)

 
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
![432618094-bf6125a8-7742-4fe5-99f6-ec98b7c75159](https://github.com/user-attachments/assets/4150ffd0-1714-480a-9f39-b9999ce80753)

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
 ![432618458-55705e99-e14a-4115-9265-3ee37c3b1171](https://github.com/user-attachments/assets/9d891092-8e1a-4abe-a8cd-087140b152b1)

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
![432618802-845ac51b-7e90-4597-bd37-ac42fa97f1ff](https://github.com/user-attachments/assets/c3bad8cd-4949-490b-a04c-0c6a30c03078)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![432619079-460cd5d1-8fae-445b-a792-f1825e06ded0](https://github.com/user-attachments/assets/2cc675de-32ae-4931-bbe8-25e898c5096f)



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
![432619341-a2c100be-3240-4f81-a102-a50b269f95d6](https://github.com/user-attachments/assets/ce66ca30-1fd2-4c7e-9662-31e385d79466)

 ./funcex.sh 
![432619459-be1ca228-9ad2-419c-9f81-ddabdda530d1](https://github.com/user-attachments/assets/934eb5ae-5ed8-4ed8-87f0-dfb4e6bddd00)

 
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
![432619779-7e9cc1cd-0a57-4764-9a35-1be41549d5ee](https://github.com/user-attachments/assets/64218b95-cf51-4ee1-bbc3-d4b7fcd2f6f6)

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
![432620384-03faac37-2742-48f2-9a95-e8af707ba948](https://github.com/user-attachments/assets/6dc849ab-00fc-43d2-9144-3fcc92e38cc8)

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
![432620669-7bc797da-f3c8-4ca9-b4d6-4c3156d11f0e](https://github.com/user-attachments/assets/61d76b70-9898-4d04-891a-6a1002394386)

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
 ![432621130-d7b4a7e9-17ee-40ad-841e-76fd7525e916](https://github.com/user-attachments/assets/7049e0f6-07ab-44f8-bb47-18c96bf665b8)

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
![432621807-fb4afc2b-262f-451f-a36e-7158fca52d2b](https://github.com/user-attachments/assets/a6b6eac9-5b8f-4fce-b3ec-5585050cd8ad)


# RESULT:
The Commands are executed successfully.
