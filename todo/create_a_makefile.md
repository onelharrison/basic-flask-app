# Create a Makefile

Create a Makefile in the root of the project's directory.

You may create the file how ever you see fit, but here are some options.

- using the touch command
    ```
    touch Makefile
    ```
- using a CLI text editor such as vim or nano
    ```
    vim Makefile

    # OR

    nano Makefile
    ```
- using a GUI text editor or IDE such as Visual Studio Code or Sublime Text


Regardless of how you choose the create the Makefile, do a simple check to ensure that it was
successfully created.

You can do this using the `ls` command while in the root of the project's directory.

```
ls
```

You should see the `Makefile` listed along side other files and directories in the root of the project's directory.

For example,

```
Makefile main.py Pipfile Pipefile.lock README.md src/ todo/
```

### make install

Add a make target named `install` to the Makefile that will install the necessary dependencies for running the application.

The commands for installing the dependencies for this application is the following.

```
python -m pip install -U pip
python -m pip install pipenv
python -m pipenv install
```

Copy the following into the Makefile to add the `install` target that uses the above commands.

```
install:
	python -m pip install -U pip
	python -m pip install pipenv
	python -m pipenv install
```

Note that the indentation done here is done using TAB. This is important. If you try to use SPACE,
your Makefile will NOT work.

Save the Makefile. Always be saving!

Now you can run `make install` to install all the necessary dependencies for running the application.

### make run

Add a make target named `run` to the Makefile that will run the application server.

The command for running the application is the following.

```
python -m pipenv run python main.py
```

Now you can run `make run` to start a server for the application.

### make clean

Add a make target named `clean` to the Makefile that will remove the resources created by the `install` make target.

The `python -m pipenv install` command creates a isolated virtual environment specifically to run the code for this project.

The virtual environment does takes up some space on your computer, so having too many of them could lead to your storage being filled up.

When you're done working on a project, it's good practice to clean up after yourself.

If you don't yet know what virtual environments are and what problems the solve, don't worry about it for now. You can make a note to
read up on it later.

The command to clean up the virtual environment created by pipenv is the following.

```
python -m pipenv --rm
```

If you test the `make clean` command, you will need to rerun the `make install` command to then be able to use `make run` to start the application server.

## Reflection

By now you may have noticed that the `install` and `run` make targets summarize the steps in the [README](/README.md) to get the project up and running.

## Reminder

Make sure to save your work by committing the Makefile you created and pushing it to your repo.

```
git add Makefile
git commit -m "Replace this with a message about what you're committing"
git push origin master
```

## Help

Checkout https://makefiletutorial.com/ to learn more about makefiles, but note that only the first page is relevant for the scope of this task.
