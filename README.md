# Python-Thermal-Printer Module

Python3 port of the original Adafruit [Python-Thermal-Printer](https://github.com/adafruit/Python-Thermal-Printer) library.

Modified to support the USB version of the printer. 

## Getting Started

Install Raspbian Buster and setup the printer according to [this](https://learn.adafruit.com/networked-thermal-printer-using-cups-and-raspberry-pi/connect-and-configure-printer).

Run a test to see if the printer is working by punching in these commands into the terminal.

``` shell
echo -e "This is a test.\\n\\n\\n" > /dev/usb/lp0
```

### Installing

Update the system and install prerequisites.

``` shell
sudo apt-get update
sudo apt-get install git cups wiringpi build-essential libcups2-dev libcupsimage2-dev python-pil python-unidecode
```

Install the printer driver. Don't worry about the warnings that g++ gives.

``` shell
git clone https://github.com/adafruit/zj-58
cd zj-58
make
sudo ./install
```

Restart the system. Clone this repository edit *printertest.py* to have the location of your printer and try to run it.

``` shell
git clone https://github.com/bubbletill/ada-receipt-printer/
cd Python-Thermal-Printer
python3 printertest.py
```

Let me know if you have any issues.
