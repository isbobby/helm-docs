# Getting Started
## M1 Configurations
To install packages using `homebrew`, the following may be required.

```arch -x86_64 /usr/local/homebrew/bin/brew install <sometool>```

This is because Homebrew needs to be installed in two places on Apple silicon: in /usr/local for rosetta-emulated (Intel) code, and /opt/homebrew for ARM64. After installing two `homebrew`s, you need to specify which `homebrew` to run. The above command executes `homebrew` with 

After installing the packages using the above command, the package binaries will be found under `/user/local/homebrew/bin`. This has to be appended to the `PATH` variable so `bash` knows where to look for these packages. To do so, add the following line to `User/user_name/.zshrc`.

`export PATH=/usr/local/Homebrew/bin:$PATH`

Then, run `source .zshrc` under `User/user_name`. Echoing the path should log out the newly updated variable.