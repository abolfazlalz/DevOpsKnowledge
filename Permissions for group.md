In this article i don't want talk about permissions and deep talk about that.

But I want to show the things that I use myself.

I always create groups for my projects and services folders.

like this:

```bash
addgrp groupname
```

Then we add permission to folder:

```bash
chmod 775 -R /path/to/project
chgrp groupname -R /path/to/project
```

In this command, we assign full access to users in __groupname__ group.

If you want assign a group to user, run below command:

```bash
usermod -aG groupname username
```

### Directory path

In my last project i work as a laravel developer. So i put my Laravel project to `/var/www/` directory.

Put your project and service directory into your user home i think is not a good idea.
but you can make a link from main project path to your home path like beow:

```bash
ln -s /path/to/projectname ~/projectname
```

this command make a link from project path to your user home directory.