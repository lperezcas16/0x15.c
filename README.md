# Simple Shell, Checks

There will be no checks released before the deadline. We **strongly** encourage the whole class to work together and create a suite of checks covering both regular tests and edged cases for each task.

Here is an example on how to check your shell.
Fork this repo and add more checks to help you and the rest of the class build the best simple shell possible.

## Configuration

Open the file `config` and update the variable `SHELL` with your shell.

## Run

Usage `./check_simple_shell.bash`

# Manual tests
##  Ctrl + D
For this test, we want to compare the behavior when pressing Ctrl + D in the following cases

### Case 1:
type a command and press Ctrl + d twice
(must be pressed twice for the shell to continue)
<br/>
##### example original shell (command sh)
`& ls`

after of press ctrl+d twice
output
`$ lslearning_shell      mini_shell  repos-github  shell_testing  simpleshell  test-c`
`$`
`vagrant@vagrant-ubuntu-trusty-64:~$`

we see that the list of files prints a new prompt and exits

### case 2
testing with a command that doesn't exist
`$ noexist`

press ctrl+d twise
output
`$ noexistsh: 1: noexist: not found`
`$`
`vagrant@vagrant-ubuntu-trusty-64:~$`

followed by the command prints the error, then a new prompt and exits

## Arrows test
This test will be compared the output in the case of arrows and enter

#### Press arrow up and enter:
`$ ^[[A`

**OUTPUT ORIGINAL SHELL:**
`$ ^[[A : not found`
`$ : 5:`

Compare with your OUTPUT and test with other arrows.
the number means the number of times that the commands is executed
this number could vary

#### Press Down and enter:
`$ ^[[B`
`sh: 3: : not found`
#### Press Left and enter:
`$ ^[[D`
`sh: 4:: not found`
` `
#### Press Right and enter:
`$ ^[[C`
`sh: 5:  : not found`