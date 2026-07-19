# 53S8-Hexadecimal-Keypad
53S8 Hexadecimal Keypad 5x3 Is a serial/parallel Keypad interface for 8-bit computers using only 7400 logic chips

## Features:
- UART interface on a IDC 3x2 connector.
- RS232 interface on a DB9 connector.
- Parallel interface on a IDC 6x2 connector.
- 5x6 hexadecimal keypad, pressing two keys will load the 8 bit register with a single byte
- Two extra keys for Carrige return and backspace, pressing CR or Backspace will fill the 8bit register with 0x0D or 0x08 respectively.  
- once the register is full the keypad will set the byteready pin to HIGH and wait for the register to be read.

## Reading the keypad:
- The register can be read via the parallel port by:
  1 - Reading the 8 parallel bits when the pin BYTE_RDY is High
  2 - Then reseting the register by setting KEYPAD_RST to HIGH

- The register can be read on the serial ports via RS232 or UART by:
  1 - Setting #SERIAL_EN LOW. 
  2 - Reading the Serial output.
  (boundrate can be set using a jumper)
  (boundrate Clock pin is also available on UART port)

### This circuit hasn't been tested yet.

## License:
This project is MIT licensed.
