Generating a new SSH key and adding it to the ssh-agent
=======================================================
New features updated 
> Enter same passphrase again: [Type passphrase again]
Adding your SSH key to the ssh-agent
Bsm,kjnjksd
sm;lmsd;lmkgf
fm;elf;le

,;lsm;mg
efore adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and generated a new SSH key.
If you have GitHub Desktop installed, you can use it to clone repositories and not deal with SSH keys.
1. Ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in "Working with SSH key passphrases", or start it manually:
# start the ssh-agent in the background
$ eval "$(ssh-agent -s)"
> Agent pid 59566
2. Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_ed25519 in the command with the name of your private key file.
$ ssh-add ~/.ssh/id_ed25519
3. Add the SSH key to your account on GitHub. For more information, see "Adding a new SSH key to your GitHub account."
Generating a new SSH key for a hardware security key
If you are using macOS or Linux, you may need to update your SSH client or install a new SSH client prior to generating a new SSH key. For more information, see "Error: Unknown key type."
1. Insert your hardware security key into your computer.
2. Open Git Bash.
3. Paste the text below, substituting in the email address for your account on GitHub.
$ ssh-keygen -t ed25519-sk -C "your_email@example.com"
Note: If the command fails and you receive the error invalid format or feature not supported, you may be using a hardware security key that does not support the Ed25519 algorithm. Enter the following command instead.
$ ssh-keygen -t ecdsa-sk -C "your_email@example.com"
4. When you are prompted, touch the button on your hardware security key.
5. When you are prompted to "Enter a file in which to save the key," press Enter to accept the default file location.
> Enter a file in which to save the key (/c/Users/you/.ssh/id_ed25519_sk):[Press enter]
6. When you are prompted to type a passphrase, press Enter.
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
7. Add the SSH key to your account on GitHub. For more information, see "Adding a new SSH key to your GitHub account."
