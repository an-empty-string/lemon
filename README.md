## lemon
Downloading, configuring, and compiling a lot of packages is terrible, especially
when you are in development and might need to do that often. `lemon` solves the problem.
Just write a `Lemonfile` like so:

```
https://github.com/some/repository.git a-folder-name ./some && ./configuration && commands && make && make install
https://github.com/some/other-repository.git a-different-folder-name ./some && ./configuration && commands && make && make install
https://github.com/some/even-more-repository.git a-new-folder-name ./some && ./configuration && commands && make && make install
```

Then `./lemon grab Lemonfile` to clone those repositories, followed by `./lemon build Lemonfile`
to compile and install your packages. Everything is done in `/tmp/lemon-$USER`,
including build logging.
