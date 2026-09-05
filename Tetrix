# TryHackMe — Game Hacking: The Game

## Overview

Completed the **Game Hacking: The Game** challenge on TryHackMe.

The objective was to analyze a Windows executable and uncover hidden data contained within the game's code.

## Skills & Techniques

- Static analysis
- Windows PE executable analysis
- String extraction
- Command-line analysis
- Basic reverse engineering

## Tools Used

- Kali Linux
- `file`
- `strings`
- `grep`

## Methodology

### 1. Identify the executable

I first used the `file` command to determine what type of executable I was working with:

file Tetrix.exe

The output identified Textrix.exe as a 64-bit Windows PE executable

### 2. Extract Readable Strings

strings Tetrix.exe

### 3. Search for Relevant Strings

Rather than manually reviewing all of the extracted strings, I filtered the output for keywords commonly associated with CTF flags and sensitive information:

strings Tetrix.exe | grep -iE 'flag|thm|secret|cipher|encrypt|decrypt'

This search revealed the flag contained within the executable

### What I learned 

This challenge demonstrated how basic static analysis can reveal useful information from an executable without needing to execute it.

I also learned how file, strings, and grep can be combined to quickly identify an executable's characteristics and search large amounts of extracted data for relevant information.
