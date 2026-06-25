iOS 15 5G Carrier Bundle Enabler (Türk Telekom / Turkey)
A complete guide to enabling official 5G settings and UI switches on iOS 15 devices for Türk Telekom (Turkey).

Normally, official 5G support for Türk Telekom was introduced in iOS 16.4+ (Carrier Bundle version 54.0+). On iOS 15, loading this bundle leaves you without the 5G menu toggles. This project fixes that by patching the carrier configuration files.

📥 Download Patched File
AVEA_tr_5G_iOS15.ipcc
 (Pre-patched carrier bundle, ready to install)
🔓 Method 1: For Jailbroken Devices (Recommended)
This is the easiest method. Since jailbreak allows modifying cellular signature checks, you can flash the .ipcc file directly.

Requirements:
A jailbroken iPhone (12 or newer) running iOS 15.
CommCenter Patch installed (Disables signature checks for carrier bundles so your phone accepts modified IPCC files).
Steps:
Install CommCenter Patch from your package manager (Sileo/Cydia).
Connect your iPhone to your PC/Mac.
Open iTunes / Finder (or 3uTools).
Hold Shift (Windows) or Option (Mac) and click Update Carrier Settings or Restore iPhone (choose carrier configuration files option).
Select the downloaded AVEA_tr_5G_iOS15.ipcc file.
Reboot your device. Go to Settings > Cellular > Voice & Data and select 5G.
🛡️ Method 2: For Non-Jailbroken Devices (TrollStore)
If you are not jailbroken, you cannot install modified .ipcc files through iTunes because of signature verification. However, you can manually replace the carrier bundle files using TrollStore.

Requirements:
TrollStore installed on your iOS 15 device.
Filza File Manager (TrollStore version) or carrier-changing tools like TrollFools / CarrierChanger.
Steps:
Extract the AVEA_tr_5G_iOS15.ipcc file (it is just a ZIP archive; rename it to .zip to extract).
Copy the Payload/AVEA_tr.bundle folder to your device.
Open Filza (TrollStore version) on your iPhone.
Navigate to:
text

/var/mobile/Library/Carrier Bundles/iPhone/
Replace the contents of the existing AVEA_tr.bundle (or com.apple.AVEA_tr.bundle) with the files from the patched bundle.
Navigate to:
text

/var/mobile/Library/Carrier Bundles/Overlay/
Find the plist overrides starting with device+carrier+... matching your carrier configuration, or replace files matching the override plists inside the patch.
Go to Settings > General > Transfer or Reset iPhone > Reset and select Reset Network Settings.
Once your phone reboots, the 5G switch should appear under Voice & Data.
