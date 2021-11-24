Test monorepo publish to github packages

We have deployed a git repo specific key using `ssh-keygen`,
registered on github via project specific settings/deply-keys,
and use that to push.

`~/.ssh/config` contains
```
Host gh-testscope
        Hostname github.com
        IdentityFile=/home/user/.ssh/key-testscope
```
so that this line can be used to push:
```
git push git@gh-testscope:craigphicks/testscope.git
```

