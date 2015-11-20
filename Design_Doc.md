# Design Doc

This is a document for laying out the requirements and necessary overarching design for a continuous integration system capable of replacing the current Node.js Jenkins setup as described in [nodejs/build](https://github.com/nodejs/build) and found at [ci.nodejs.org](https://ci.nodejs.org/).

# Requirements

It must be able to fully replace the current Jenkins setup, including:

- Capable of executing tasks on an extremely wide variety of remote machines, including but not limited to only using `ssh` to access and run commands on the machine.
 - Platforms including but not limited to: Windows, OS X, Linux (many varities), Solaris, AIX.
 - Architectures including but not limited to: x86, x64, armv{6,7,8}, ppcle, ppcbe.
- Able to have nested subtasks, parallel and sequential.

# Features

In addition to meeting the requirements, the CI should aim to have:

- Less technical overhead and required domain knowledge than Jenkins.
- Readable status reports with indicators of multiple failure types beyond test failures, including disconnects.
- Comparable status reports to easily search for failure changes.
