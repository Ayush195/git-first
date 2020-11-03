# Generating a new SSH key

    (1) Open Git Bash.
    (2) Paste the text below, substituting in your GitHub email address.

    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    This creates a new ssh key, using the provided email as a label.

    > Generating public/private rsa key pair.
    [Image]


# Adding your SSH key to the ssh-agent

    (1) If you have GitHub Desktop installed, you can use it to clone repositories and not deal   with SSH keys.

    Ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in "Working with SSH key passphrases", or start it manually:

    # start the ssh-agent in the background
    $ eval $(ssh-agent -s)
    > Agent pid 59566
    [Image]

    (2) Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.

    $ ssh-add ~/.ssh/id_rsa
    [Image]


# Adding a new SSH key to your GitHub account


    (1) Copy the SSH key to your clipboard.

    If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.

    $ clip < ~/.ssh/id_rsa.pub
    # Copies the contents of the id_rsa.pub file to your clipboard

    (2) In the upper-right corner of any page, click your profile photo, then click Settings
    [Image]

    (3) In the user settings sidebar, click SSH and GPG keys.
    [Image]

    (4) In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air"

    (5) Paste your key into the "Key" field.
    [Image]

    (6) Click Add SSH key.
    [Image]

    (7) If prompted, confirm your GitHub password.
    [Image]