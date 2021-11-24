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

To make this be used automatically on push
```
git remote remove origin  # in case origin is already set
git remote add origin git@gh-testscope:craigphicks/testscope.git
git push --set-upstream origin master
```
Thereafter 
```
git push 
```
is sufficient


