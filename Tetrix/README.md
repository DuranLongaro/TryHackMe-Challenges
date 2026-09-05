# TryHackMe — Game Hacking: The Game

## What I Did

This challenge involved analyzing a Windows executable (`Tetrix.exe`) to find a hidden flag.

I downloaded the challenge files and moved the executable into my Kali Linux VM.

## Analysis

First, I checked what type of executable I was dealing with:

file Tetrix.exe

This identified it as a 64-bit Windows PE executable.

I then used strings to extract readable text from the binary:

(`strings Tetrix.exe`)

There was a lot of output, so I narrowed the search using grep:

(`strings Tetrix.exe | grep -iE 'flag|thm|secret|cipher|encrypt|decrypt' `)

This revealed the flag directly in the executable.

Tools used: Kali Linux, file, strings, grep

My Takeaway: This was a good introduction to static analysis. I learned that before jumping into more complicated reverse-engineering tools, it's worth checking whether useful information is already exposed through readable strings.
