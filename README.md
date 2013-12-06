pam_imap
========

**Introduction**

PAM module that authenticates against a remote IMAP or IMAPS server. Supports multiple servers, SSL, password caching, user blacklists, and many configuration abilities.

The original module itself is unmaintained, the purpose of this repository is to keep the module working with the latest versions of Linux.

**Dependencies**
```
libpam0g-dev
build-essentials
gcc
libssl
make
libcrypto
etc
```

These will be different depending on your distro.

**Build**
```
git clone https://github.com/MrDroid/pam_imap/
cd pam_imap
chmod +x *
./configure
make clean
make
```

**Install**

```
...
```
