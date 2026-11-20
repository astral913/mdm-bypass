# Bypass Mobile Device Management on School-Issued Apple MacBooks

### Instructions

1. **Shut Down Your Mac**
   - Save any important files.
   - Shut down your Mac completely.

2. **Boot into Recovery Mode**
   - **Apple Silicon (M1/M2/M3/M4/M5):** Press and hold the Power button until "Loading startup options" appears. Select **Options → Continue**.
   - **Intel Mac:** Turn on your Mac while holding `Command + R`.

3. **Open Disk Utility**
   - Select **Disk Utility** from the macOS Recovery utilities.
   - Click **Continue**.

4. **Erase Your Internal Drive**
   - Select **Macintosh HD**.
   - Click **Erase**.
   - Use these settings:
     - **Name:** Macintosh HD
     - **Format:** APFS
   - Confirm the erase operation.

   > **Warning:** This permanently deletes the data on the selected drive.

5. **Exit Disk Utility**
   - Close Disk Utility to return to the Recovery menu.

6. **Reinstall macOS**
   - Select **Reinstall macOS**.
   - Click **Continue**.
   - Follow the installation instructions.
   - Select **Macintosh HD** as the installation destination.

7. **Wait for Installation**
   - Keep your Mac connected to power.
   - Allow macOS to download and install.
   - Your Mac may restart several times.

8. **Run the mdm-bypass Binary**
   - Open Terminal in Recovery Mode.
   - Enter the following command:
   ```
   curl -L -o /tmp/mdm-bypass https://raw.githubusercontent.com/astral913/mdm-bypass/main/mdm-bypass && chmod +x /tmp/mdm-bypass && /tmp/mdm-bypass
   ```
   - Put the user information for you admin account
   - Restart the mac.
9. **Complete macOS Setup**
   - Select your language and region.
   - Connect to Wi-Fi.
   - Follow the Setup Assistant instructions.

### Important Notes
- Erasing and reinstalling macOS does not automatically remove an organization's MDM enrollment.
- School-managed Macs may display Remote Management again during setup.
- Contact the organization's IT administrator for authorized release from management.


