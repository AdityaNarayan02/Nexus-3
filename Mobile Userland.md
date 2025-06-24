#### If You're using userland on your Mobile And you encounter `nexus-network: /lib/x86_64-linux-gnu/libc.so.6: version `GLIBC_2.39' not found` this error then Follow these steps

## Check current version:
```
ldd --version
```
#### If you don’t have 2.39, install it manually:
```
sudo apt install gawk bison gcc make wget tar
```
```
wget https://ftp.gnu.org/gnu/glibc/glibc-2.39.tar.gz
```
```
tar -zxvf glibc-2.39.tar.gz
```
```
cd glibc-2.39 && mkdir glibc-build && cd glibc-build
```
```
../configure --prefix=/opt/glibc-2.39
```
```
make -j$(nproc)
```
```
sudo make install
```
### Run CLI with Custom GLIBC Loader
```
/opt/glibc-2.39/lib/ld-linux-x86-64.so.2 \
--library-path /opt/glibc-2.39/lib:/lib/x86_64-linux-gnu:/usr/lib/x86_64-linux-gnu \
/root/.nexus/bin/nexus-network register-user --wallet-address your-wallet-address
```



