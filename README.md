# Workflow-test-
Repository used for the workflow test & implementation (before separating the task) : https://github.com/BaseMax/github-actions-compile-c

The GitHub Action is configured to automatically compile the C program every time a change is pushed to the main branch or a pull request is created.

Create a new file in the .github/workflows directory:

    File name: c-compile.yml
    Action Setup: The action is defined in the c-compile.yml file, which runs the following steps:  Name an action Build
        Checkout code using the actions/checkout@v4 action.
        Compile the C program using gcc -o my_program main.c.
        Upload the program in a file (named my_program )

        Name an action test
        specify that it uses previous task Build
        Checkout code using the actions/checkout@v4 action
        Download code using the actions/download-artifact@v4 action
        Give the execution permission for running linux/windows requirement)
        Run the compiled program and ensure that it works.
