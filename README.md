# Profiles REST Api

Profiles rest api course code


###Steps to push project in git hub.We need to start by creating a public private key pair. 

Go to terminal or git bash window where the git is initiated and run the following commands.

## ls ~/.ssh  ---> Just to make sure we dont have any existing keys in our SSH directory.
By default the SSH directory is where all public private SSH keys are created on the system and this should be 
same for Mac or if you're using Windows with git bash.

### ssh-keygen -t rsa -b 4096 -C "amaniitmandi59@gmail.com" ---> This runs the ssh-key gen tool and then it says it wants to create a new key with a type "RSA" with 
4096 bytes and then "-C" and "amaniitmandi59@gmail" is just the comment so we can identify what key this is for if we ever need to check it.Okay so if you hit enter, it will
generate the key pair and by default it will create it in your home directory "(/c/Users/Aman/.ssh/id_rsa)". "id_rsa" is the default key for your system.

Creating a pass phrase for the key adds an extra layer of security on your key so if somebody manages to steal the key from the computer they wont be able to use
it without the paraphrase.

The key has now been saved in --->  /c/Users/Aman/.ssh/id_rsa.pub

##ls ~/.ssh --->  id_rsa    id_rsa.pub
id_rsa--> this file here is the private key. Never share the contents with this key or the file with anyone else.
id_rsa.pub--> This is the public key this is the key that you can upload to services like github in order to authenticate.

##Now go to github.com and add the public key to our account.Steps are given below:
1.Go to settings.
2.Click on SSH and GPG navigation tables
3.Click on "NEW SSH KEY" button.

Now go back to gitbash or terminal and run the command to output our public key-->  "cat ~/.ssh/id_rsa.pub" and press enter.
Now copy the randon string of text here ending in the comment we provided in the capital -C part of our command in the earlier steps. So this is our public key.

4.Paste the string in the "key" text box in the github. enter the title "aman-laptop".

OK now that we've setup authentication, we should be able to push the project to github.

5.Create a new repository.
Go to terminal and run --> 

git remote add origin git@github.com:kumarAman-1792/profiles-rest-api.git

git push -u origin master

passphrase- Aman123!@ and press enter 

Here's the message from git terminal->

## branch 'master' set up to track 'origin/master'. ###