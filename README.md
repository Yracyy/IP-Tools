# IP Tools

A single-page, client-side toolkit for common IP addressing tasks, subnet calculation, address format conversion, IP range expansion, and a CIDR quick-reference table. No frameworks, no build step, no server calls.

**[Live Demo](https://yracyy.github.io/IP-Tools/)**

## Features

### 🧮 Subnet Calculation
Enter an IP + CIDR prefix (e.g. `192.168.1.100 /24`) and instantly get:
- Network address, broadcast address, usable host range
- Subnet mask, wildcard mask, total & usable host counts
- A bit-level binary visualization showing where the network/host boundary falls

### 🔄 Converter
- **IP → other formats**: dotted decimal to decimal (uint32), hexadecimal, octal, and binary
- **Reverse lookup**: paste a decimal, hex (`0xC0A80101`), or 32-bit binary string and get the dotted-decimal IP back

### 📋 IP Range Expander
Enter a start and end IP and get every address in between listed out with decimal/binary equivalents and Network/Broadcast/Host tagging. Capped at 65,536 addresses to keep the browser responsive.

### 📊 CIDR Reference Table
Full `/0` through `/32` table — subnet mask, wildcard mask, and usable host count for every prefix length. Click any entry to copy its subnet mask.


## Usage

Download `index.html` and open it directly in any browser. No installation needed.

## Notes on the math

- IPs are converted to 32-bit unsigned integers for all calculations, using bitwise operations (`>>>`, `<<`) rather than string manipulation — this is the same approach used internally by real networking tools.
- The binary visualization directly shows the network/host bit split, which is the core concept subnet masking is built on.

## License

MIT
