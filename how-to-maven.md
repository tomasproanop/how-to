# Manually install Apache Maven on a Mac (without using Homebrew)

**Download Apache Maven:**
Go to the Apache Maven download page and download the latest version of Maven. Choose the binary tar.gz file (e.g., apache-maven-3.8.4-bin.tar.gz).

**Extract the Maven archive:**
Once the download is complete, navigate to the directory where the Maven archive was downloaded. Open Terminal and run the following command to extract the contents of the tar.gz file:

python

    tar -xzvf apache-maven-3.8.4-bin.tar.gz

Move Maven to a suitable directory:
After extracting, move the Maven folder to a location of your choice. You can move it to /usr/local or /opt directory. For example:

bash

    sudo mv apache-maven-3.8.4 /usr/local

**Configure environment variables:**
Open the .bash_profile or .bashrc file in your home directory using a text editor like nano or vim:

bash

    nano ~/.bash_profile

Add the following lines to the file:

bash

    export M2_HOME=/usr/local/apache-maven-3.8.4
    export PATH=$M2_HOME/bin:$PATH

Save the file and exit the text editor. Then, run the following command to apply the changes:

bash

    source ~/.bash_profile

Verify installation:
Open a new Terminal window and run the following command to verify that Maven is installed correctly:

    mvn -v

This command should display the Maven version and other information if the installation was successful.
