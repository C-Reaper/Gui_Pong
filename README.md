# Project README

## Overview
This project is a simple implementation of the game Pong in C. It utilizes a custom library `Windowlib` for handling window and rendering operations, which includes functionalities such as creating windows, updating the screen, clearing the screen, and managing user input.

The project supports building on multiple platforms: Linux, Windows (using MinGW-w64), Wine (Linux cross-compilation for Windows), and WebAssembly using Emscripten.

## Features
- **Multi-platform Support**: The game can be compiled and run on Linux, Windows, and Web.
- **Basic Game Mechanics**: Pong with two paddles controlled by the user and an AI opponent (on some platforms).

## Project Structure
### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries:
  - `Windowlib` for window and rendering operations.
  - For Linux: X11 and PNG libraries (`libX11`, `libpng`)
  - For Windows: MinGW-w64
  - For WebAssembly: Emscripten

## Build & Run
### Linux
1. Navigate to the project directory:
   ```sh
   cd /path/to/Gui_Pong
   ```
2. Build the project:
   ```sh
   make -f Makefile.linux all
   ```
3. Clean and rebuild:
   ```sh
   make -f Makefile.linux clean
   make -f Makefile.linux all
   ```
4. Run the game:
   ```sh
   make -f Makefile.linux exe
   ```

### Windows (using MinGW-w64)
1. Navigate to the project directory:
   ```sh
   cd /path/to/Gui_Pong
   ```
2. Build the project:
   ```sh
   make -f Makefile.windows all
   ```
3. Clean and rebuild:
   ```sh
   make -f Makefile.windows clean
   make -f Makefile.windows all
   ```
4. Run the game:
   ```sh
   make -f Makefile.windows exe
   ```

### Wine (Linux cross-compilation for Windows)
1. Navigate to the project directory:
   ```sh
   cd /path/to/Gui_Pong
   ```
2. Build the project:
   ```sh
   make -f Makefile.wine all
   ```
3. Clean and rebuild:
   ```sh
   make -f Makefile.wine clean
   make -f Makefile.wine all
   ```
4. Run the game:
   ```sh
   WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
   ```

### WebAssembly (Emscripten)
1. Navigate to the project directory:
   ```sh
   cd /path/to/Gui_Pong
   ```
2. Build the project:
   ```sh
   make -f Makefile.web all
   ```
3. Clean and rebuild:
   ```sh
   make -f Makefile.web clean
   make -f Makefile.web all
   ```
4. Run the game (open `build/index.html` in a web browser):
   ```sh
   make -f Makefile.web exe
   ```

This README provides a straightforward guide to building and running the Pong game on various platforms using the provided makefiles.