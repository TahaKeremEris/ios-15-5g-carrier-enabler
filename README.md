# iOS 15 5G Carrier Bundle Enabler (Turk Telekom / Turkey)

A complete guide to enabling official 5G settings and UI toggles on iOS 15 devices for Turk Telekom (Turkey).

Official 5G support for Turk Telekom was introduced in iOS 16.4+ (Carrier Bundle version 54.0+). On iOS 15, loading this bundle can leave the 5G menu toggles unavailable. This project addresses that by patching carrier configuration files.

## Download Patched File

- [AVEA_tr_5G_iOS15.ipcc](./AVEA_tr_5G_iOS15.ipcc) (pre-patched carrier bundle, ready to install)

## Method 1: Jailbroken Devices (Recommended)

This is the easiest method. Since jailbreak allows modifying cellular signature checks, you can flash the `.ipcc` file directly.

### Requirements

- A jailbroken iPhone (12 or newer) running iOS 15
- CommCenter Patch installed (disables signature checks for carrier bundles)

### Steps

1. Install CommCenter Patch from your package manager (Sileo/Cydia).
2. Connect your iPhone to your PC or Mac.
3. Open iTunes / Finder (or 3uTools).
4. Hold `Shift` (Windows) or `Option` (Mac), then click **Update Carrier Settings** (or the equivalent carrier configuration option).
5. Select `AVEA_tr_5G_iOS15.ipcc`.
6. Reboot your device.
7. Go to **Settings > Cellular > Voice & Data** and select **5G**.

## Method 2: Non-Jailbroken Devices (TrollStore)

If you are not jailbroken, you cannot install modified `.ipcc` files through iTunes due to signature verification. You can still replace carrier bundle files manually using TrollStore-based tools.

### Requirements

- TrollStore installed on iOS 15
- Filza File Manager (TrollStore version) or tools like TrollFools / CarrierChanger

### Steps

1. Extract `AVEA_tr_5G_iOS15.ipcc` (it is a ZIP archive; rename to `.zip` first).
2. Copy `Payload/AVEA_tr.bundle` to your device.
3. Open Filza (TrollStore version) on your iPhone.
4. Navigate to:

```text
/var/mobile/Library/Carrier Bundles/iPhone/
```

5. Replace the contents of `AVEA_tr.bundle` (or `com.apple.AVEA_tr.bundle`) with the patched files.
6. Navigate to:

```text
/var/mobile/Library/Carrier Bundles/Overlay/
```

7. Find override plist files starting with `device+carrier+...` that match your carrier configuration, and replace them with the patched override plists.
8. Go to **Settings > General > Transfer or Reset iPhone > Reset**, then choose **Reset Network Settings**.
9. After reboot, the 5G option should appear under **Voice & Data**.
