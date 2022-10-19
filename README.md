# Udemy - Complete Guide to Protocol Buffers 3 [Java, Golang, Python] 2021-9

# Introduction 

## the need for protocol buffers

**Evolution of data**

**csv**

![1](./images/1.png)

![2](./images/2.png)

**Relational tables definitions**

![3](./images/3.png)

**JSON**

![4](./images/4.png)

**Protocol Buffers**

![5](./images/5.png)
![6](./images/6.png)
![7](./images/7.png)

## How are Protocol Buffers used

![8](./images/8.png)
![9](./images/9.png)

**Proto2 vs Proto3**

![10](./images/10.png)

-------------------------

# Protocol Buffers Basics 1

![11](./images/11.png)

## Scalar Types 

**Number**

![12](./images/12.png)

**Boolean**

![13](./images/13.png)

**String**

![14](./images/14.png)

**Bytes**

![15](./images/15.png)

**Summary: Types**

![16](./images/16.png)

## Tags 

![17](./images/17.png)
![18](./images/18.png)

## Repeated Fields

![19](./images/19.png)

## Comments

![20](./images/20.png)

## Default Values for fields

![21](./images/21.png)

## Enums

![22](./images/22.png)

-------------------

# Protocol Buffers Basics

## Defining Multiple Message in the same .proto file

![23](./images/23.png)

## Nesting Types

![24](./images/24.png)

## Importing Types

![25](./images/25.png)

## Packages

![26](./images/26.png)

---------------
# setting up protoc compiler

```text

In order to perform code generation, you will need to install protoc on your computer.

============ MacOSX =============

It is actually very easy, open a command line interface and type brew install protobuf

============ Ubuntu (Linux) ============

Find the correct protocol buffers version based on your Linux Distro:https://github.com/google/protobuf/releases

Example with x64:

# Make sure you grab the latest version
curl -OL https://github.com/google/protobuf/releases/download/v3.5.1/protoc-3.5.1-linux-x86_64.zip
# Unzip
unzip protoc-3.5.1-linux-x86_64.zip -d protoc3
# Move protoc to /usr/local/bin/
sudo mv protoc3/bin/* /usr/local/bin/
# Move protoc3/include to /usr/local/include/
sudo mv protoc3/include/* /usr/local/include/
# Optional: change owner
sudo chown [user] /usr/local/bin/protoc
sudo chown -R [user] /usr/local/include/google
============ Windows============

Download the windows archive:https://github.com/google/protobuf/releases

Example:https://github.com/google/protobuf/releases/download/v3.5.1/protoc-3.5.1-win32.zip

Extract all to C:\proto3

Your directory structure should now be

C:\proto3\bin

C:\proto3\include

Finally, add C:\proto3\bin to your PATH:

From the desktop, right-click My Computer and click Properties.
In the System Properties window, click on the Advanced tab
In the Advanced section, click the Environment Variables button.
Finally, in the Environment Variables window (as shown below), highlight the Path variable in the Systems Variable section and click the Edit button. Add or modify the path lines with the paths you wish the computer to access. Each different directory is separated with a semicolon as shown below.

C:\Program Files; C:\Winnt; ......; C:\proto3\bin
(you need to add; C:\proto3\bin at the end)
```

`protoc -I=proto --go_out=go .\proto\person.proto`


```text
If you want to follow along with me, please have the following:

- Golang installed:https://golang.org/doc/install

- VSCode Installed

- The VSCode Golang extension:https://code.visualstudio.com/docs/languages/go

- The source code for this project (download / star the project):https://github.com/simplesteph/protobuf-example-go

- Golangpackages:

go get -u github.com/golang/protobuf/protoc-gen-go
go get -u github.com/golang/protobuf/proto
- Protoc Compiler (see Setting up Protoc Compiler Section)
```

------------------

# Data Evolution with Protobuf

## The need for updating the protocols

![27](./images/27.png)
![28](./images/28.png)
![29](./images/29.png)

## Updating Protocol Rules

![30](./images/30.png)

9-3