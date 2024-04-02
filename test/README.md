# How to Test [WORK IN PROGRESS]

## General Guidance

The JobSet testing process is based on the [upstream Kubernetes one](https://github.com/kubernetes/community/blob/f8e7444dea53d0eb9a29304e367a72abc4b1abba/contributors/devel/sig-testing/testing.md#testing-guide).
If you are interested in more context on why things are done certain ways,
checking the Kubernetes repo is a good place to start. Feel free to ask
questions on the [JobSet repo](TODO) as well.

## Instructions on Testing
You can test JobSet on bare metal or using containers.
We recommend using containers whenever possible.

### How To Test Using Containers

TODO

### How to Test Using Bare Metal
1. Complete the steps in the JobSet contributer setup guide[LINK].
2. Make your changes.
3. Follow the [testing process](#general-testing-steps) entering the commands
directly as is into your command line. 
4. There are now two main possibilities:
   1. You have no errors! In which case, feel free to submit your
   changes for review (or don't it's up to you!).
   2. You have a lot of errors (or maybe just a few) in front of you!
   Congrats, welcome to the fun of debugging! If you get stuck,
   feel free to ask for help on the repo.
5. That is all.


### <a name="general-testing-steps"></a> General Testing Steps

Perform the following steps to update the documentation and
run tests.

1. `make generate` to do SOMETHING
2. running the different test types.
   1. `make test` to do something
   2  `make test-python-sdk` to do something
   3. `make test-integration` to do something
   4. `make test-e2e-kind` to do something
3. `make verify`
    * Ensure you have a clear workspace before running
    `make verify`. In particular `git diff` should show
    no output. If `make verify` fails afterwards and there
    are file changes, run `git commit` to commit those changes
    and run `make verify` again.
