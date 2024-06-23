---
layout: post
title: Chapter 01 - Introduction to Computers, Programs, and Python
categories: [COSC1436]
tags: [notes, python]
---

### Contents

1. [Introduction](#introduction)
2. [What is a Computer?](#what-is-a-computer)
    1. [Central Processing Unit](#central-processing-unit)
    2. [Bits and Bytes](#bits-and-bytes)
    3. [Memory](#memory)
    4. [Storage Devices](#storage-devices)
3. [Programming Languages](#programming-languages)
    1. [Machine Language](#machine-language)
    2. [Assembly Language](#assembly-language)
    3. [High-Level Languages](#high-level-languages)
4. [Operating Systems](#operating-systems)

### Introduction

The term <span class="code green">**programming**</span> means to create (or to develop) software, also called a <span class="code green">**program.**</span>  
Software contains the instructions that tell a computer or device what to do.  

Software developers create software with tools called <span class="code green">**programming languages.**</span>

### What is a Computer?

*A computer is an electronic device that stores and processes data.*

A computer consists of the following major hardware components:
- central processing unit
- memory
- storage devices (e.g. disks, CDs)
- input devices (e.g. mouse, keyboard)
- output devices (e.g. monitors, printers)
- communication devices (e.g. modems, network interface cards)

These components are interconnected by a subsystem called a <span class="code green">**programming languages.**</span>  
A bus is a system of "roads" that run among the computer's components. In personal computers, the bus is built into the computer's <span class="code green">**motherboard**</span>, a circuit case that connects all the parts of a computer together.


#### Central Processing Unit

The computer's central processing unit retrives instructions from memory and executes them.  

##### Components of CPU

It usually has two components:
- A control unit
- And an arithmetic / logic unit

The control unit cooardiantes the actions of the other components.  
The arithmetic / logic unit performs <span class="code blue">numeric operations</span> (addition, subtraction) and <span class="code blue">logical operations</span> (comparisons).

CPUs are built on small, silicon semiconductor chips.  
They contain millions of tiny, electric switches called <span class="code green">**transistors**</span>, used to process information.

##### Clock Speed

Every computer has an internal clock that emits electronic pulses at a constant rate.  
The pulses are used to control and synchronize the pace of operations.  

Clock speed is measured in *hertz (Hz)*, where 1 Hz is 1 pulse per second.  
> *A higher clock speed enables more instructions to be executed in a given period of time.*

Intel's newest processor runs at 3 GHz, which is 3 billion pulses per second.

##### CPU Cores

The <span class="code green">core</span> of a CPU peforms the reading and executing of instructions.  
Some CPUs are now produced with multiple cores to increase processing power.

#### Bits and Bytes

Computers store information in a series of 1s and 0s. These 1s and 0s are interpreted as digits in the binary number system.

| Binary | Decimal |
|--------|---------|
| 00     | 0       |
| 01     | 1       |
| 10     | 2       |
| 11     | 3       |

A single digit of either a 0 or 1 is a bit.  
A byte consists of 8 bits.

#### Memory

A computer's <span class="code green">memory</span> consists of an ordered sequence of bytes for storing programs and its data.  
A program and its data must be moved int othe computer's memory before they can be executed by the CPU.  

> *Memory can be considered as the computer's working area for executing a program.*

Every byte in memory has a <span class="code blue">unique address</span>, which is used to located the byte for storing and retrieving.  
Because the bytes in memory can be accessed in any order, the memory is also referred to as <span class="code green">random-access memory (RAM).</span>

| Memory Address | Value         |
|----------------|---------------|
| 0x0001         | 00101010 (42) |
| 0x0002         | 11111111 (255)|
| 0x0003         | 10000000 (128)|
| 0x0004         | 01001011 (75) |

#### Storage Devices

Data in RAM is lost when a system is powered off.  
Data must be saved into a <span class="code green">storage device</span> for permanent storage.

##### Types of Storage Devices

- Hard Disk Drives and Solid-State Drives
- Optical disk drives (CD and DVD)
- USB flash drives

<span class="code green">Drives</span> are devices that operate storage media like disks and CDs. A storage medium physically stores data and programs.  
The drive reads from and writes data to the medium.


### Programming Languages

*Computer programs, known as software, are instructions that tell a computer what to do.*

#### Machine Language

A computer's native language is its <span class="code blue">machine language</span>, which is a set of built-in primitive instructions.  
The instructions are in the form of binary code.

To add two numbers in machine language, you may have to write an instruction that looks like this:  

<span class="code">1101101010011010</span>

#### Assembly Language

<span class="code blue">Assembly language</span>, referred to as a <span class="code blue">low-level language</span>, was created as an alternative to machine language.  
It uses a mnemonic to represent each machine-language instruction.  
To subtract two numbers in assembly code, it may look like this:  

<span class="code">add 2, 3, result</span>  

Because computers cannot execute assembly language, an <span class="code blue">assembler</span> is used to translate assembly language to machine language.

<iframe style="border:none" width="100%" height="250" src="https://whimsical.com/embed/H21WxWFj8mfpDUbmtCZQzW"></iframe>  

#### High-Level Languages

High-level langauges are programming languages that are:
- platform independent
- easy-to-learn

They write instructions in the form of statements. For example:

<span class="code">area = 5 * 5 * 3.14159</span>

This code would calculate the area of a circle with the radius of 5.


A program written in a high-level language is called a <span class="code blue">source program</span> or <span class="code blue">source code.</span>

Because computers cannot execute source code, it must be translated using a <span class="code blue">compiler</span> into machine code.

### Operating Systems

The operating system manages and controls a computer's activities.

<iframe style="border:none" width="100%" height="250" src="https://whimsical.com/embed/HXWeVNpa1ZkftLr6aS8Ns5"></iframe>  

The major tasks of an operating system are:
- Controlling and monitoring system activites
- Allocating system resources
- Scheduling operations