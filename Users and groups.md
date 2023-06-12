Work with a Linux server with root user is never a good idea. 

So we have to create a user for ourselves.

its too easy and just need a single line command:

> Replace your username `abolfazl` to your username in this article.

```bash
adduser abolfazl
```

Now we have a user that named `abolfazl`.

### Add to sudo users

For add sudo access to your user, we need to add the user to the sudo group.

```bash
usermod -aG sudo abolfazl
```

Done.