# Vermonster laptop customizations

This is a starter `~/.laptop.local` for Vermonster developers.

1. Place the `.laptop.local` file in your home directory
2. Customize the list of Homebrew and Cask packages as desired
3. **[Run thoughtbot's laptop script][laptop]**
4. It will install both the standard set of packages and our customizations

* In case you want to set a laptop for multiple users, you may want to add permissions for `homebrew`.
This will allow any users in an admin group can manage `homebrew`. For more info, [here][gist]

```bash
# allow admins to manage homebrew's local install directory
$ chgrp -R admin /usr/local
$ chmod -R g+w /usr/local

# allow admins to homebrew's local cache of formulae and source files
$ chgrp -R admin /Library/Caches/Homebrew
$ chmod -R g+w /Library/Caches/Homebrew

# if you are using cask then allow admins to manager cask install too
$ chgrp -R admin /opt/homebrew-cask
$ chmod -R g+w /opt/homebrew-cask
```

[gist]: https://gist.github.com/jaibeee/9a4ea6aa9d428bc77925
[laptop]: https://github.com/thoughtbot/laptop#install
