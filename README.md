# MiniOS

A minimal operating system implementation written in C and assembly. This project demonstrates the fundamental concepts of operating system development, including boot process, kernel initialization, memory management, and basic system utilities.

## Project Structure

- `boot/` - Bootloader and early initialization code
- `include/` - Header files and system definitions
- `init/` - System initialization code
- `kernel/` - Core kernel functionality
- `lib/` - System libraries and utilities
- `mm/` - Memory management implementation
- `tools/` - System tools and shell implementation

## Building the Project

### Prerequisites

- GCC (with 32-bit support)
- NASM (Netwide Assembler)
- Make
- QEMU (for running the OS)

### Build Instructions

1. Clone the repository:
```bash
git clone https://github.com/TanishTunwal/MiniOS.git
cd MiniOS
```

2. Build the project:
```bash
make
```

3. Run the OS in QEMU:
```bash
make run
```

## Usage

Once the OS boots, you'll see a shell prompt (`minios $ `). Available commands:

- `help` - Display available commands
- `clear` - Clear the screen
- `echo [text]` - Print text to console
- `halt` - Halt the system
- `reboot` - Restart the system

## Features

- **Kernel Implementation**: Core kernel with interrupt handling and system calls
- **Memory Management**: Basic paging implementation with 4KB pages
- **Shell Interface**: Interactive shell with commands (help, clear, echo, halt, reboot)
- **Hardware Support**: 
  - VGA text mode console output
  - PS/2 keyboard input with scan code conversion
  - Programmable Interval Timer (PIT) for system timing
- **System Initialization**: Complete boot process from bootloader to userspace
- **Error Handling**: Comprehensive trap and exception handling
- **Multitasking Foundation**: Basic scheduler framework (expandable)

## Development

The project is built using:
- C (GNU99 standard)
- x86 Assembly (NASM)
- 32-bit architecture

### Build System

The project uses a Makefile-based build system with the following main targets:
- `make` - Build the entire project
- `make clean` - Clean build artifacts
- `make run` - Run the OS in QEMU
- `make backup` - Create a backup of the project

## License

This project is licensed under the GPL-3.0 License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- Thanks to all contributors who have helped shape this project
- Inspired by various OS development tutorials and resources