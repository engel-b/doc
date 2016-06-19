# Releasing maven artifacts

## Github

### Checking for existing SSH keys 

Check if there are any existing SSH keys.

1. Open Git Bash
2. Enter `ls -al ~/.ssh` to see if existing SSH keys are present:
>ls -al ~/.ssh
># Lists the files in your .ssh directory, if they exist

By default, the filenames of the public keys are one of the following:

* id_dsa.pub
* id_ecdsa.pub
* id_ed25519.pub
* id_rsa.pub

_[Checking for existing SSH keys][1]_

### Generating a new SSH key and adding it to the ssh-agent

1. Open Git Bash
2.
>ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
># Creates a new ssh key, using the provided email as a label
>Generating public/private rsa key pair.
3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
>Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
4. At the prompt, type a secure passphrase. For more information, see "Working with SSH key passphrases".
>Enter passphrase (empty for no passphrase): [Type a passphrase]
>Enter same passphrase again: [Type passphrase again]

_[Generating a new SSH key and adding it to the ssh-agent][2]_

[1]: https://help.github.com/articles/checking-for-existing-ssh-keys/
[2]: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/