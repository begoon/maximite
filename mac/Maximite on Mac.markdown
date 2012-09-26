Maximite on Mac
===============

Check USB setting: "Top Menu -> About This Mac"

![](maximite-settings-about.png)

Click on "More Info..."

![](maximite-settings-system-report.png)

Click on "System Report...", then click on "USB" on the left.

![](maximite-normal-usb-mode.png)

If Maximite is in the normal mode, you should see "Maximite" under "USB Bus" on the right.

![](maximite-bootloader-usb-mode.png)

If Maximite is in the bootloader mode ("LOAD FIRMWARE" button was pressed at powering on and the greed LED is now flashing), you should see "Silicon Chip Bootloader" under "USB Bus" on the right.

When Maximite (in the normal or bootloader mode) is connected via USB cable to your Mac and visible via USB settings, there should be a device created automatically named `/dev/cu.usbmodem<some_number>`, for example `/dev/cu.usbmodem411`.

![](miximite-usb-modem.png)

Now you can get connected to Maximite via a terminal program (for example, minicom, which can be installed via Homebrew as `brew install minicom` in the terminal).

Start the terminal window and run minicom by:

    minicom -b 115200 -D /dev/cu.usbmodem411
    
This command sets the port baud rate to 115200 and device name to `/dev/cu.usbmodem411`.

If everything is correct, you should get a Maximite MM-Basic prompt in your terminal window:

![](maximite-mmbasic-prompt.png)

Now you can try typing something in MM-Basic:

![](maximite-test-program.png)
