# Makefile for aBlink

TARGET	= aBlink

ASRCS 	= $(wildcard *.S)
INTTBL	= FALSE

# board definition
MCU	= atmega328p
F_CPU	= 16000000

# do not modify anything below this line
ifeq ($(OS),Windows_NT)
	include /usr/local/include/Makefile.win
	PORT = COM6
else
	UNAME_S = $(shell uname -s)
	ifeq ($(UNAME_S), Linux)
		include /usr/local/include/Makefile.unx
		PORT = /dev/ttyACM0
	endif
	ifeq ($(UNAME_S), Darwin)
		include /usr/local/include/Makefile.mac
		PORT = /dev/cu.usbmodem1411
	endif
endif
