# Template for CircuitPython on Raspberry Pi Pico on PyCharm

The steps for using this template are in this order.

1. [Copy this repo as a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) or [using the command line:](https://stackoverflow.com/questions/62630485/is-it-possible-to-create-a-new-git-repository-from-a-template-only-using-the-com)
   - git clone \<link> 
   - remove the .git folder
   - git init .
   - git add .
   - git commit -m "Commit from template"
   - git push -u origin master
   

2. If the MicroPython plugin for PyCharm is not installed, install it.
   - Go to File &#8594; Settings &#8594; Plugins &#8594; Marketplace
   - Search for MicroPython and install it.


3. Download the CircuitPython UF2 file for the pico from Raspberry Pi [downloadable UF2](https://circuitpython.org/board/raspberry_pi_pico/). This can also be found in this project.<br>
**Note, that the file in this project might not be the newest version.**


4. Push and hold the BOOTSEL button and plug your Pico into the USB port of your Raspberry Pi or other computer. Release the BOOTSEL button after your Pico is connected.


5. It will mount as a Mass Storage Device called RPI-RP2.


6. Drag and drop the CircuitPython UF2 file onto the RPI-RP2 volume. Your Pico will reboot. You are now running CircuitPython.

7. Now enable the MicroPython plugin
   - Go to File &#8594; Settings &#8594; Languages & Frameworks &#8594; MicroPython
   - **&#9745; Enable MicroPython support**
   - Set Device type &#8594; **Raspberry Pi Pico**
   - Set Device path: COM_<br> 
     _Example: COM1_
   - Press **OK** to confirm.


8. Stop PyCharm from auto-saving.
   - Go to File &#8594; Settings &#8594; Appearance & Behaviour &#8594; System Setting
   - Turn off: <br>
     &#9744; **Save files if ...** <br>
     &#9744; **Save files when ...** <br>
   

9. Now add an extra content root
   - Go to File &#8594; Settings &#8594; Project [YOUR_PROJECT_NAME] &#8594; Project Structure
   - Click **+ Add Content Root** and select the drive letter of the Pico, normally named: "**CIRCUITPY**" eg. **D:/**
   - Note, you are using the **CIRCUITPY** to work in, when saved the Pico will run the new code.


10. Now go to Python Packages and install the [circuitpython-stubs](https://pypi.org/project/circuitpython-stubs/)


11. If additional packages are needed they can now be installed as well.


12. If you want to see the results such as print() in your console go to:
    - Tools → MicroPython → MicroPython REPL <br>
    - If nothing is showed:
      - Check the COM port
      - press ctrl+D the soft restart the program. <br>


## Useful links
[CircuitPython](https://circuitpython.org//) <br>
[CircuitPython - Docs](https://circuitpython.readthedocs.io/en/latest/docs/index.html) <br>
[CircuitPython - Book](https://cdn-learn.adafruit.com/downloads/pdf/circuitpython-essentials.pdf) <br>
[Adafruit - Welcome to CircuitPython](https://learn.adafruit.com/welcome-to-circuitpython) <br>
[Adafruit - PyCharm and CircuitPython](https://learn.adafruit.com/welcome-to-circuitpython/pycharm-and-circuitpython) <br>
