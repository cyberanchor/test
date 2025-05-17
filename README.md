## Сompiling 3proxy, frp on Android (Termux, ARM64)

### verify architecture
check the device architecture to confirm ARM64 (`aarch64`):
```bash
uname -om
```
**output**: `aarch64 Android`

---

### compiling 3proxy 


##### install packages
install required tools and dependencies:

```bash
pkg update -y; pkg upgrade -y
pkg install git make clang build-essential -y
```


##### compile
clone and build 3proxy:

```bash
git clone https://github.com/z3APA3A/3proxy
cd 3proxy
ln -s Makefile.Linux Makefile
make
```

**output**: binaries in `3proxy/bin/`


---


**3proxy compiling process on termux:**

<div align="center">
    <video src="files/3proxy.mp4" autoplay muted loop controls width="600" height="600" alt="3proxy compiling process on termux"></video>
</div>


---


### frp compilation

##### install packages
install required tools for frp:

```bash
pkg update -y; pkg upgrade -y
pkg install git golang make -y
```

##### compile
clone and build frp:

```bash
git clone https://github.com/fatedier/frp
cd frp
make
```

**output**: binaries in `frp/bin/`


**frp compiling process on termux:**

<div align="center">
    <video src="files/frp.mp4" autoplay muted loop controls width="600" height="600" alt="frp compiling process on termux"></video>
</div>





---