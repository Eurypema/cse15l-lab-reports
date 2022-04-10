# Lab Report 1

## Step 1: Installing VCode

Go to the Visual Studio Code website and follow the instructions to download and install it on your computer: 
[Link](https://code.visualstudio.com/)

Once one installs VSCode (downloading the installer as per one's OS), the following should pop up:

![image](https://user-images.githubusercontent.com/103284133/162596646-427d4b10-aa60-4a0f-82af-1b56b8fe0b54.png)

## Step 2: Connecting Remotely

Install OpenSSH if one is on Windows first:
[Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

First look up one's course-specific account for CSE15L here:
[Link](https://sdacs.ucsd.edu/~icc/index.php)

Now open a terminal in VSCode. In it, enter
```
$$ ssh cs15lsp22zz@ieng6.ucsd.edu
```
where zz stands for the letter combination for one's course-specific account.

The first time one does so, this prompt should appear:

![image](https://user-images.githubusercontent.com/103284133/162596888-ed1ee703-f21a-4112-8591-4444f44de481.png)

Enter 'yes'. After this, one shall be prompted for the password. Enter it as per usual and the following should be observed:

![image](https://user-images.githubusercontent.com/103284133/162596918-3a123efc-acae-4429-90a7-d52240031b57.png)

## Step 3: Using Commands

The commands
```
$$ cd X
```
and
```
$$ ls
```
change the directory to X and list the contents of the directory, as so:

![image](https://user-images.githubusercontent.com/103284133/162597372-6af844fb-4aa6-4da2-b193-5fc220ef7ffd.png)

Adding a tilda after cd returns one to the home directory. Adding the modifiers -l, -a, and -t after ls produces the following results:

![image](https://user-images.githubusercontent.com/103284133/162597468-37616279-c31d-47e1-ae39-099966ca417c.png)

Combining these modifiers produces the following:

![image](https://user-images.githubusercontent.com/103284133/162597481-3a73cb97-e719-416a-b43f-800f18041f07.png)

There are other commands to try, such as 
```
$$ cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
$$ cat /home/linux/ieng6/cs15lsp22/public/hello.txt
```
but these require special permissions be granted.

## Step 4: Moving Files Over SSH

Create a file WhereAmI.java with contents that follow:
```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
The following command then copies WhereAmI to a specified remote computer:
```
$ scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/
```
where, as again, zz is a placeholder for whatever letter combination of the remote computer that you wish to save it to. The result should look something like this:

![image](https://user-images.githubusercontent.com/103284133/162600461-c59b1b7f-d43d-4c3f-834c-8c7fd1a22997.png)

Entering the command 'exit' logs out of the remote computer.

## Step 6: 

On one's local machine, enter the following command:
```
$ ssh-keygen -t ed25519
```
When prompted on where to save the RSA key pair, enter /Users/XX/.ssh/id_rsa, where XX refers to one's username.

Afterwards, when prompted for a passphrase, enter none. Something like this should appear:

![image](https://user-images.githubusercontent.com/103284133/162600603-db35b2ae-dece-410c-a475-2815de77b9cf.png)

Going onto the remote machine, enter the following command:
```
$ mkdir .ssh
```

On one's local machine, enter the command
```
$ scp /Users/gordo/.ssh/id_rsa.pub cs15lsp22afl@ieng6.ucsd.edu:~/.ssh/authorized_keys
```
Enter the password when prompted, and now log into the remote machine (logout first if one has not). One will discover now that no password needs be provided now when accessing that remote machine.

## Step 7: Making Remote Running Even More Pleasant

It may be noted that:
1. One can use semicolons to run multiple commands on the same line in most terminals.
2. One can write a command in quotes at the end of an ssh command to directly run it on the remote machine.

Allow it to be supposed that one had made a change to a file and would like to save it to the remote machine. Then
