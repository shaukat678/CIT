---
---

# 🧑‍💻 Computer Fundamentals — Level 2

## Lesson 1: What Actually Happens When You Turn On a Computer?

You've probably pressed the power button thousands of times without thinking about what happens.

There's actually a sequence.

### Step 1 — Power

Electricity reaches the computer's components.

The CPU can't simply start executing your applications immediately. The computer first needs to initialize its hardware.

### Step 2 — Firmware starts

The motherboard contains firmware, commonly called **UEFI** on modern PCs.

It performs early hardware initialization and determines how the computer should start.

You may hear the older term **BIOS**. BIOS and UEFI aren't exactly the same thing, but BIOS is still commonly used informally to refer to this firmware layer.

### Step 3 — Find something to boot

The firmware identifies a bootable device, such as an SSD.

### Step 4 — Bootloader

A **bootloader** helps load the operating system.

Conceptually:

```text
Power
  ↓
Firmware
  ↓
Bootloader
  ↓
Operating System
  ↓
Login screen
  ↓
Desktop
```

### Step 5 — Operating system loads

The OS loads important components into memory.

Now the computer can provide the normal environment you're familiar with.

---

# Lesson 2: What Is Actually Running?

Once your computer is on, **many things are running simultaneously**.

You might think:

> "I'm running Chrome."

But underneath Chrome, the operating system is managing:

* Chrome
* graphics
* audio
* networking
* storage
* background services
* security
* input devices
* system processes

You can think of it like:

```text
                 OPERATING SYSTEM
                        │
        ┌───────────────┼────────────────┐
        ↓               ↓                ↓
     Chrome          Music            Files
        │
        ↓
     Internet
```

---

# Lesson 3: Processes

A **process** is a running instance of a program.

For example, when you open a calculator application, the operating system creates a process for it.

You can have:

```text
Chrome
Calculator
Music player
File manager
```

all running at the same time.

The operating system keeps track of them.

---

# Lesson 4: Programs vs Processes

These aren't quite the same.

### Program

Software stored on your computer.

### Process

A program that is currently executing.

Analogy:

> A recipe is like a program.
> Someone actually cooking the recipe is like a process.

One program can sometimes create multiple processes.

---

# Lesson 5: How Does the CPU Run Programs?

At the simplest level, the CPU repeatedly:

1. gets instructions
2. interprets them
3. performs operations
4. continues to the next instructions

A simplified model:

```text
Fetch
  ↓
Decode
  ↓
Execute
  ↓
Repeat
```

Modern CPUs are vastly more sophisticated than this simple model, but this is a useful starting point.

---

# Lesson 6: What Is a Bit?

Computers ultimately represent information using **bits**.

A bit can have two states:

```text
0
1
```

You can think of it as:

> off/on

or:

> false/true

A computer doesn't literally store everything as tiny switches in the simplistic sense, but binary representation is fundamental to digital computing.

---

# Lesson 7: Bytes

A group of **8 bits** is called a byte.

```text
1 byte = 8 bits
```

For example:

```text
10101100
```

is 8 bits.

You'll encounter:

* KB
* MB
* GB
* TB

when dealing with storage and memory.

---

# Lesson 8: KB, MB, GB, TB

These represent increasingly large amounts of digital information.

Very roughly:

```text
KB → thousands of bytes
MB → millions of bytes
GB → billions of bytes
TB → trillions of bytes
```

There are technical differences between decimal and binary measurement systems, so don't worry about exact conversions yet.

For beginners, the important idea is:

> **GB is larger than MB, and TB is larger than GB.**

---

# Lesson 9: How Can a Computer Store a Photo?

A photo looks like a picture to you.

To a computer, it's data.

The image is represented digitally using numbers.

Those numbers describe things such as:

* pixel positions
* colors
* brightness
* image structure

For example, an image might contain millions of pixels.

Each pixel has information describing its color.

---

# Lesson 10: How Does Text Become Data?

Your computer also represents text digitally.

For example:

```text
A
B
C
```

are represented using numerical codes.

Modern systems commonly use **Unicode**, which allows computers to represent characters from many writing systems.

That's why your computer can handle things like:

```text
Hello
سلام
你好
こんにちは
```

---

# Lesson 11: What Is RAM Actually Doing?

Suppose you open a browser.

The browser's program and the data it needs are loaded into memory.

Then you open a document.

More information is loaded.

Then another application.

More information.

So RAM is constantly being used by the operating system and applications.

Conceptually:

```text
RAM
├── Operating system
├── Browser
├── Document
├── Background services
└── Other applications
```

---

# Lesson 12: What Happens When RAM Is Full?

The operating system needs ways to manage memory when programs need more memory than is immediately available.

It can move some data between RAM and storage.

This is often called **virtual memory**.

Storage is much slower than RAM, so excessive memory pressure can make a computer feel slow.

---

# Lesson 13: Why Does an SSD Make a Computer Feel Faster?

Imagine two computers with similar CPUs and RAM.

One has a traditional HDD.

The other has a fast SSD.

The SSD can generally access data much more quickly.

That can make things like:

* booting
* launching applications
* opening files

feel significantly faster.

---

# Lesson 14: What Is a GPU Really Doing?

Suppose a game needs to display:

```text
🌳 trees
🏠 buildings
💡 lighting
👤 characters
🌎 environment
```

The GPU performs enormous amounts of graphics-related computation.

The result eventually becomes pixels displayed on your screen.

Very simplified:

```text
Game
 ↓
CPU + GPU
 ↓
Graphics calculations
 ↓
Frame
 ↓
Monitor
```

---

# Lesson 15: CPU vs GPU

A simple beginner distinction:

### CPU

General-purpose computing.

### GPU

Highly parallel computation, especially useful for graphics and certain other workloads.

Don't think:

> CPU = important, GPU = only for games.

Modern GPUs are used for many computational tasks.

---

# Lesson 16: What Is a Driver?

A **driver** is software that allows the operating system to communicate appropriately with particular hardware.

For example:

```text
Operating System
       ↓
    Driver
       ↓
   Graphics hardware
```

Other devices also use drivers.

Without appropriate software support, an OS may not be able to use a hardware device properly.

---

# Lesson 17: Plugging in a USB Device

Suppose you plug a USB keyboard into your computer.

Conceptually:

```text
Keyboard
   ↓
USB connection
   ↓
USB controller
   ↓
Operating system
   ↓
Keyboard driver/support
   ↓
Applications
```

You press `A`.

The application receives an input event and can display:

```text
A
```

---

# Lesson 18: Ports

Your computer may contain physical ports such as:

* USB-A
* USB-C
* HDMI
* DisplayPort
* Ethernet
* audio connectors

Different ports support different kinds of connections and capabilities.

**USB-C is a connector shape, not one single speed or capability.**

This is important because two USB-C ports can support different features.

---

# Lesson 19: Filesystems

We're going deeper now.

Your SSD doesn't simply contain a giant pile of files.

The operating system uses a **filesystem** to organize stored data.

Examples include:

* NTFS
* APFS
* ext4

The filesystem keeps track of things such as:

* file names
* directories
* metadata
* where data is stored
* permissions

Think of it as the organizational system used to manage the storage device.

---

# Lesson 20: File Metadata

A file contains more than just its visible content.

Its metadata may include things such as:

* name
* size
* creation information
* modification time
* permissions
* location

For example:

```text
Report.docx
Size: 2.4 MB
Modified: 2026-09-18
```

---

# Lesson 21: Permissions

Operating systems need to control who can access what.

A file might have permissions determining who can:

* read it
* modify it
* execute it

This becomes particularly important in multi-user systems and servers.

---

# Lesson 22: Why Does the OS Need Permissions?

Imagine a computer where every program could modify anything it wanted.

A malicious application could potentially modify important system files.

Permissions help limit what users and programs are allowed to do.

This is part of computer security.

---

# Lesson 23: User Accounts

Your computer can have multiple user accounts.

For example:

```text
Computer
├── Dad
├── Mom
├── Student
└── Guest
```

Each account can have its own:

* files
* settings
* preferences
* permissions

---

# Lesson 24: Administrator Accounts

An administrator has elevated privileges.

That means they can perform actions ordinary users may not be allowed to perform.

For example:

* installing certain software
* changing system settings
* modifying protected areas

You should not automatically approve administrator prompts without understanding what you're allowing.

---

# Lesson 25: Why Does Your Computer Ask for Permission?

Suppose an application says:

> "Allow this application to make changes?"

The OS is asking for authorization because the operation may require elevated privileges.

Don't develop the habit of clicking **Yes** automatically.

Ask:

> What is this application trying to do, and did I expect it?

---

# Lesson 26: Now Let's Return to the Internet

We know:

```text
Your computer
 ↓
Router
 ↓
ISP
 ↓
Internet
 ↓
Server
```

But how does your computer actually communicate?

Through **protocols**.

---

# Lesson 27: What Is a Protocol?

A protocol is a set of rules for communication.

Humans need languages and conventions to communicate.

Computers need standardized rules too.

Examples:

* IP
* TCP
* UDP
* DNS
* HTTP
* HTTPS
* TLS

---

# Lesson 28: TCP and UDP

Two important transport protocols are:

### TCP

Designed for reliable, ordered delivery.

Useful when accurate delivery matters.

### UDP

Connectionless and lightweight, without TCP's same reliability mechanisms.

Can be useful where speed, latency, or application-controlled delivery behavior matters.

Examples of workloads can include real-time communication and certain games.

---

# Lesson 29: The Internet Has Layers

Networking becomes easier to understand if you think in layers.

A simplified view:

```text
Application
    ↓
Transport
    ↓
Internet
    ↓
Link
    ↓
Physical
```

Different networking technologies and models use slightly different terminology, but the layered idea is extremely useful.

---

# Lesson 30: What Happens When You Watch a Video?

Let's combine everything.

You click **Play**.

### 1

The application/browser processes your action.

### 2

It communicates with a remote service.

### 3

DNS may be used to resolve domain names.

### 4

Network protocols establish/maintain communication.

### 5

Data is sent through networks.

### 6

Packets arrive at your device.

### 7

Your computer processes the data.

### 8

The CPU/GPU and other hardware handle the required work.

### 9

The display shows the resulting frames.

### 10

Your speakers/headphones produce audio.

All of this happens extremely quickly.

---

# Your Next Practical Assignment

Don't just read the next lessons.

Open your computer and practice these:

### Exercise 1

Open your file manager.

Find:

* Documents
* Downloads
* Pictures
* Desktop

Understand where they are.

### Exercise 2

Create:

```text
Computer Practice
```

Inside it create:

```text
Documents
Images
Test
```

### Exercise 3

Create a text file called:

```text
my_first_file.txt
```

Write a few sentences.

Save it.

### Exercise 4

Copy it.

Rename the copy:

```text
my_second_file.txt
```

### Exercise 5

Move the second file into:

```text
Computer Practice/Test
```

### Exercise 6

Delete it.

Then restore it from your system's Trash/Recycle Bin.

### Exercise 7

Open your browser and practice:

```text
Ctrl + T
Ctrl + L
Ctrl + F
Ctrl + W
Ctrl + Shift + T
```

### Exercise 8

Search for something you're interested in.

Then identify:

**Which part is the browser?**

**Which part is the search engine?**

**What is the URL?**

**What is the domain?**

---

## Next lesson

After this, the natural next step is **"Networking from absolute zero"** — where we'll build a detailed picture of:

**Wi-Fi → router → IP → MAC → DNS → TCP/UDP → ports → packets → routing → NAT → ISP → servers → HTTP/HTTPS**

That will make the Internet section much easier to understand.
