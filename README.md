# awesome-ctf-wargame

**Writeup oriented CTF skill improvement**

The corresponding ctf problem and wargame will be curated based on each required skill. 
:exclamation:  You may need the login account for browsing each wargame properly.

## [*] System hacking / Pwnable

### Basic introduction

- [Pwning Pwnables](https://dc416.com/wp-content/uploads/2016/07/Session-2-Harold-Rodriguez-Pwning-pwnables.pdf)

###  Wargames :pencil: 

| Difficulty | Wargames | 
|------------|----------|
| Easy | [(Exploit-exercise) Protostar](https://exploit-exercises.com/protostar/) |
| Medium | [(Root-me) App System](https://www.root-me.org/en/Challenges/App-System/), [(PwnerRank) Binary Exploitation](https://www.pwnerrank.com/categories/binary-exploitation/) |
| High | [Pwnable.kr](http://pwnable.kr/) |

### [+] BoF (Buffer Overflow)

- Overwrite local variable
    - [Easy | x86] : [(Protostar) Stack0](https://exploit-exercises.com/protostar/stack0/), [(Protostar) Stack1](https://exploit-exercises.com/protostar/stack1/), [(root-me) x86 BoF basic1](https://www.root-me.org/en/Challenges/App-System/ELF-x86-Stack-buffer-overflow-basic-1)
- Environment variable usage
    - [Easy | x86] : [(Protostar) Stack2](https://exploit-exercises.com/protostar/stack2/), [(root-me) x86 basic4](https://www.root-me.org/en/Challenges/App-System/ELF-x86-Stack-buffer-overflow-basic-4)
- Overwrite EIP (to be other function like flag printing)
    - [Easy | x86] : [picoctf-2013/rop1](https://github.com/ctfs/write-ups-2013/tree/master/pico-ctf-2013/rop-1),  [(Protostar) Stack3](https://exploit-exercises.com/protostar/stack3/), [(Protostar) Stack4](https://exploit-exercises.com/protostar/stack4/), [(root-me) x86 BoF basic2](https://www.root-me.org/en/Challenges/App-System/) 
    - [Easy | x64] : [(root-me) x64 BoF basic](https://www.root-me.org/en/Challenges/App-System/ELF-x64-Stack-buffer-overflow-basic)

### Overwrite EIP + shellCode injection

| Technique | Knowledge     |  Best Training :thumbsup: |
|-----------|---------------|-----------|
| shellcode injection | **shellcode**   | [pico-ctf-2013/overflow-4](https://github.com/ctfs/write-ups-2013/tree/master/pico-ctf-2013/overflow-4)  |


- [Easy | x86] : [(Protostar) Stack5](https://exploit-exercises.com/protostar/stack5/)

### Ret2PLT, Ret2Libc, ROP

- [Easy | x86] : [pico-ctf-2013/rop2](https://github.com/ctfs/write-ups-2013/tree/master/pico-ctf-2013/rop-2)


### Threat Mitigation Bypass

#### ASLR : **Mem Leak**

| Technique | Knowledge     |  Best Training :thumbsup: |
|-----------|---------------|-----------|
| ASLR Bypass | **ROP, Mem leak**  |  [pico ctf 2013/rop3](https://github.com/ctfs/write-ups-2013/tree/master/pico-ctf-2013/rop-3)         |

#### Canary

#### PIE

| Technique | Knowledge     |  Best Training :thumbsup: |
|-----------|---------------|-----------|
| Address Calac  | **ROP, Mem Leak, Address offset** | [defcon 2015 / r0pbaby](https://github.com/ctfs/write-ups-2015/tree/master/defcon-qualifier-ctf-2015/babys-first/r0pbaby) |


### [+] Format String

#### Arbitrary memory read

#### Direct Parameter Access (`n$`)

#### Arbitrary memory write using `%n`

- [Easy | x86] : [Protostar: Format1](https://exploit-exercises.com/protostar/format1/) |


### [+] Heap Exploitation

[shellphish/how2heap: A repository for learning various heap exploitation techniques.](https://github.com/shellphish/how2heap) :star2: 

### [+] Exploitation technique  :star2:

![img](https://raw.githubusercontent.com/2O2L2H/awesome-ctf-wargame/master/roadmap/pwnable/pwnable.png)

[@Pwning Pwnables](https://dc416.com/wp-content/uploads/2016/07/Session-2-Harold-Rodriguez-Pwning-pwnables.pdf)

- **Jump to payload**
    - ret2reg or jump to payload if the stack is executable and addresses aren’t randomized 
- **GOT overwrite**
    - Commonly used in format string exploitation
    - Overwrite pointer in GOT with pointer to another location
- **Code re-use (ret2libc, ret2plt, ROP)**
    - Make use of existing code and instructions to exploit the binary 

### [+] TIP & Tools  :+1: 

- GDB enhancer : [2O2L2H/gdb-switcher](https://github.com/2O2L2H/gdb-switcher)
    - gef : Multi-Architecture GDB Enhanced Features for Exploiters & Reverse-Engineers : [:octocat:](https://github.com/hugsy/gef)
    - peda: PEDA - Python Exploit Development Assistance for GDB [:octocat:](https://github.com/longld/peda)
    - pwndbg: Exploit Development and Reverse Engineering with GDB Made Easy [:octocat:](https://github.com/pwndbg/pwndbg)
- Exploit frameworks
    - Generate and search pattern string for exploit development : [exploit-pattern @github](https://github.com/Svenito/exploit-pattern)
    - CTF framework and exploit development library [pwntools @github](https://github.com/Gallopsled/pwntools)
    - hellman/libformatstr: Simplify format string exploitation. [libformatstr @github](https://github.com/hellman/libformatstr)
- ROP tools
    - Ropper : find gadgets to build rop chains for different architectures (x86/x86_64, ARM/ARM64, MIPS, PowerPC) : [Ropper](https://github.com/sashs/Ropper)
    - ROPGadget : search your gadgets on your binaries to facilitate your ROP exploitation. ROPgadget supports ELF, PE and Mach-O format on x86, x64, ARM, ARM64, PowerPC, SPARC and MIPS architectures. : [ROPGadget](https://github.com/JonathanSalwan/ROPgadget)
- LIBC database
    - niklasb/libc-database: Build a database of libc offsets to simplify exploitation : [libc-database](https://github.com/niklasb/libc-database)



## [*] Cryptography

### [+] Caesar cryptography

### [+]  AES

### [+]  RSA


## [*] Forensics


## [*] Web

### [+]  SQL Injection

### [+]  XSS (Cross-site Scripting)




