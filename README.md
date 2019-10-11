# kopya
Collaborative digital library by Czyka Tumaliuan, Josefti Nito, Gladys Regalado.

# Build Your Own Library!

1. Collect your eBooks.
2. Set-up your digital library platform - device and software
* on a desktop/laptop
* on a smartphone
* on a portable server using RaspberryPi

## Desktop/Laptop
Install Calibre on your PC running Windows, Mac or Linux. Download Calibre here https://calibre-ebook.com/download. Upload your books on Calibre. To share 

## Smartphone
Install an eBook reader like MoonReader, https://www.moondownload.com/. Upload your books to your reader.

## Portable Library Server

### Hardware
* Raspberry Pi 3 Model B+ (RPi)
* RPi enclosure
* Power Supply
* MicroSD Card
* Monitor
* Keyboard
* Mouse

### Software
* Calibre
* Calibre-web
* RaspAP

### Instructions
1. Prepare SD Card with OS
2. Put together RPi
3. Install Calibre E-Library and Calibre Web
4. Upload books to Calibre
5. Set Calibre Web to start automatically
a. Create a unit file in '/lib/systemd/system/kopya.service'
'''
 [Unit]
 Description=My Sample Service
 After=multi-user.target

 [Service]
 Type=idle
 ExecStart=/usr/bin/python /home/pi/sample.py

 [Install]
 WantedBy=multi-user.target
'''
b. Set permissions of unit file
'sudo chmod 644 /lib/systemd/system/sample.service'

c. Configure systemd to start unit file during boot sequence
'sudo systemctl daemon-reload'
'sudo systemctl enable sample.service'
Reference: https://www.dexterindustries.com/howto/run-a-program-on-your-raspberry-pi-at-startup/

6. Install RaspAP
7. Connect to your Library over wifi
8. If everything works, set RPi to start without a display.
9. Start reading!

# Where to get books?
1. ProjectGutenberg, https://www.gutenberg.org/
2. Open Culture, http://www.openculture.com/free_ebooks
3. Internet Archive, https://archive.org/details/texts
4. International Children's Digital Library, http://en.childrenslibrary.org/
5. Open Library, https://openlibrary.org

