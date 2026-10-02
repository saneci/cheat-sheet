# SSH

## Table of content

1. [Generating keypair](#generating-keypair)
2. [Adding your SSH key to the ssh-agent](#adding-your-ssh-key-to-the-ssh-agent)
3. [Connect to the server](#connect-to-the-server)

## Generating keypair

1. Open Git Bash
2. Paste the text below, substituting in your email address, this creates a new SSH key, using the provided email
   as a label
    ```sh
    ssh-keygen -t ed25519 -C "{email_address}"
    ```
3. When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file
   location or enter a path to a file in which to save the key
4. Skip passphrase

## Adding your SSH key to the ssh-agent

Before adding a new SSH key to the ssh-agent to manage your keys, you should have checked for existing SSH keys and
generated a new SSH key

1. Start the ssh-agent in the background
    ```sh
    eval "$(ssh-agent -s)"
    ```
2. Add your SSH private key to the ssh-agent. If the private key is saved as `id_ed25519` in the `~/.ssh/` directory,
   add it for authentication as such
    ```sh
    ssh-add {path_to_ssh_private_key}/id_ed25519
    ```
3. Add the SSH public key to your account on GitHub. For more information, see
   "Adding a new SSH key to your GitHub account"

For more information please see
the [full documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

## Connect to the server

1. Enter the `ssh` command in the terminal
    ```sh
    ssh {user}@{server_ip_address}
    ```
