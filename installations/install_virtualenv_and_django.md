#### Install Virtualenv on Linux. 

1. Open Terminal (Applications > Utilities > Terminal)
2. Enter the following commands:
NOTE: The command `sudo` will require an admin password. The same password you use to install other programs. Typing will be hidden
    
    1. Install Pip. (Python Package Installer):

        ```
        sudo easy_install pip
        ```
    2. Install virtualenv:

        ```
        sudo pip install virtualenv
        ```

    3. Navigate to where you want to store your code. 
        Typical location for saving yoru code is in a folder/directory called "Development" so other you can keep it organized and in one place:

            ```
            mkdir Development
            cd Development
            ```

        NOTE: Using "Dropbox" or "Google Drive" is also an optional place to store your code. If you use services like this, your code will definitely sync but it's possible virtualenv might not work properly on other computers.

    4. Create a new virtualenv:

        ```
        virtualenv yourenv
        ``` 

        The name "yourenv" above is arbitrary. You can name it as you like.

    5. Activate virtualenv:

        ```
        source bin/activate
        ```
        The result in Terminal should be something like:
        ```
        (yourenv) moha@Inspiron:~/Development$
        ``` 

    6. Install Django:
        ```
        pip install django==1.9
        ```
        NOTE: If you need a differnet version, replace those numbers accordingly.

    7. Happy Coding with Django.
