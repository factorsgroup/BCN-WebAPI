Create a new repository on the command line
----------------------------------------------------------------
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:factorsgroup/BCN-WebAPI.git
git push -u origin master


Push an existing repository from the command line
----------------------------------------------------------------
git remote add origin git@github.com:factorsgroup/BCN-WebAPI.git
git push -u origin master


Changing Username/Password
----------------------------------------------------------------
$ git commit -m 'first commit'
[master (root-commit) 597e032] first commit
 Committer: unknown <ssekhon@<computer>.<network>>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 14 insertions(+)
 create mode 100644 README.md

Generate SSH Key
----------------------------------------------------------------
PROBLEM:
--------
ssekhon@<Computer-Name> /BCN-WebAPI (master)
$ git push origin master
Permission denied (publickey).

SOLUTION:
---------
ssekhon@BRIG-100453 /
$ cd bin

ssekhon@BRIG-100453 /bin
$ ssh-keygen

Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/ssekhon/.ssh/id_rsa): <Do-Not-Use-Any-Name>
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in FactorsSSH.
Your public key has been saved in FactorsSSH.pub.
The key fingerprint is:
e7:f5:8f:23:dc:56:ef:b7:ae:85:be:b8:5c:62:ca:04 ssekhon@<Computer-Name>

Make sure you have a key and SSH is using it
------------------------------------------------------------------
ssekhon@BRIG-100453 /BCN-WebAPI (master)
$ ssh-add -l
Could not open a connection to your authentication agent.

Adding SSH Key
-------------------------------------------------------------------
ssh-add path/to/key

Now copy your public key text and past it inside github.com/Admin/SSHKeys
Done!
