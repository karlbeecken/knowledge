# Flash an ESP-32 with FTDI232 board

## Steps

1. Connect (FTDI – ESP):
	- GND – GND
    - RXD – TXD
    - TXD – RXD
    - CTS/RTS – RTS/EN
    - DTR – DTR/GPIO0
2. Do _not_ connect power yet
3. Run idf.py flash
4. Wait for the RX LEDs on the FTDI board to flash
5. Plug in power just when the flashing takes a short break
6. Enjoy your code!