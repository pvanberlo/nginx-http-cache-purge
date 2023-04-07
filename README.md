# Instructions

## nginx 1.23.4

1) Get the configure options used to compile your version of nginx:

```shell
nginx -V
```

2) Install relevant packages required for compile:

```shell
apt install build-essential libpcre3-dev libssl-dev zlib1g-dev libxml2-dev libxslt1-dev libgd-dev libgeoip-dev
```

3) Apply the following patches from the patches folder:

dynamic-module.patch
segfault-1.11.6.patch

4) Compile dynamic module:

```shell
./configure --add-dynamic-module=<path to module source> <configure options from step 1>
make modules
```

The dynamic module can be found in the objs directory.

5) Copy the dynamic module to the server you wish to use it on.

