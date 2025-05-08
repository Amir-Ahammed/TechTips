# How to Install Network Drivers via USB During Windows Installation (No Internet Fix)
Scenario: You’re installing Windows on a PC/laptop, but it says "No network drivers found", and there's no internet (Wi-Fi or LAN not working).

![ChatGPT Image May 8, 2025, 10_35_28 PM](https://github.com/user-attachments/assets/33f3dba6-f578-42cf-85ca-60445ff97185)

## Step-by-Step Process:

### 1. Identify Your Network Hardware
* On another working PC:
  * Check the manufacturer and model of the target PC or its network card (Intel, Realtek, etc.).
  * Go to the official website (e.g., Dell, Lenovo, Realtek, Intel).

### 3. Download the Correct Drivers
* Download the LAN and Wi-Fi drivers for the exact model and OS version (e.g., Windows 11 - Version 21H2, 64-bit ).
* Look for `.INF`-based versions, or extractable ZIP files (not `.EXE` if you’ll use them during install).

If you have the `.INF` or extracted driver files, you may skip Step 4 and proceed directly to Step 5.

### 4. Driver Preparation (When .INF is not available directly)
* Download the `.exe` driver file from the official manufacturer’s website.
* Run the downloaded `.exe` file.
* On the setup window, click **Next** >.
* **Accept** the License Agreement if prompted.
* Choose the **“Extract”** option instead of “Install” (if available).
* Select a destination folder where the files will be extracted (`e.g., USB_Drive:\Drivers\LAN`).
* Complete the extraction process.

💡Alternative: You can also use [7-zip](https://www.7-zip.org/) to open the .exe and manually extract `.INF`, `.SYS`, and `.CAT` files to USB_Drive.

### 5. Driver Preparation (When you have the `.INF` or extracted driver files)
* Format a USB stick to FAT32 for compatibility.
* Create a folder (e.g., Drivers).
* Copy the extracted drivers (not EXE installers) into it.


### 6. Load Driver During Windows Installation
* Standard Method: On the network connection screen, you may see an “Install Driver” button.
  * Insert the USB drive containing the extracted driver files.
  * Click “Install Driver.”
  * In the file browser that appears, navigate to the folder where the `.INF` driver files are located.
  * Windows will then automatically detect and install the appropriate network driver.
  * Once the correct driver is loaded, your network adapter should appear, and the setup will allow you to connect to a network.

* Alternative Method: If the “Install Driver” option does not appear:
  * Press **Shift + F10** to open Command Prompt.
  * Type `devmgmt.msc` and press Enter to open Device Manager.
  * In Device Manager, locate **“Network Adapters”** or any **“Unknown Devices”** (often with a yellow warning icon).
  * Right-click the device and select **“Update driver”**.
  * Choose **“Browse my computer for drivers”,** then select the USB folder where the drivers are located.
  * Complete the installation and close all windows.
  * Continue with the Windows setup once the network is available.
