## Getting Started

This repository leverages Node.js to provide linting, auto-fixing, and streamline the commit process. With Node.js installed, you start up the project by running:

```
npm i
```

This will install all the Node.js dependencies and automatically register a pre-commit hook.

### How to Commit Code

Instead of using `git commit`, we prefer that you use `npm run commit`. You will understand why when you try it but basically it streamlines the commit process and helps us generate better CHANGELOGs.

### Pre-Commit Hook

Even if you decide not to use `npm run commit`, you will see that `git commit` behaives differently since the pre-commit hook is installed when you run `npm i`. This pre-commit hook is there to test your code before committing. If you need to bypass the pre-commit hook, then you will have to add the `--no-verify` tag at the end of your `git commit` command (e.g. `git commit -m "Commit" --no-verify`).

### NPM Tasks Available

With the dependencies installed, you can see a list of the available commands by running `npm run info`. This will log a help menu to the console informing you about the available commands and what they do. After running the command, you will see something that looks like this:

```
❯ npm run info

> packer-project@1.0.0 info
> npm-scripts-info

build:
  Build all of the images
build:hyperv:
  Build a Hyper-V image
build:kvm:
  Build a QEMU/KVM image
build:parallels:
  Build a Parallels image
build:virtualbox:
  Build a VirtualBox image
build:vmware:
  Build a VMWare image
commit:
  The preferred way of running git commit (instead of git commit, we prefer running 'npm run commit')
info:
  Logs descriptions of all the npm tasks
fix:
  Automatically fix formatting errors
launch:
  Runs 'vagrant up' to automatically spin up the VM
prepare-release:
  Updates the CHANGELOG with commits made using 'npm run commit'
test:
  Validates the Packer configuration file (i.e. template.json) and performs some other linting
update:
  Runs .update.sh to automatically update meta files and documentation
version:
  Used by 'npm run prepare-release' to update the CHANGELOG
```

For example, `npm run build` will run the `build` step described above. You can see exactly what each command is doing by checking out the `package.json` file.
