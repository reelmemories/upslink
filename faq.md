# UPSLink FAQ

## What is UPSLink?

UPSLink is an Android application that monitors UPS devices through NUT (Network UPS Tools) and compatible `upsd` servers.

UPSLink provides battery status, runtime estimates, power event notifications, widgets, and monitoring tools directly from your Android device.

---

## What UPS systems are supported?

UPSLink supports any UPS exposed through a compatible NUT (Network UPS Tools) server.

Common supported environments include:

* Synology NAS
* Unraid
* Proxmox
* TrueNAS
* Raspberry Pi
* Linux servers running NUT

---

## Does UPSLink require an account?

No.

UPSLink works without:

* Account creation
* Cloud registration
* Subscription services

Your UPS connections and settings are stored locally on your device.

---

## Does UPSLink support notifications?

Yes.

UPSLink can provide notifications for:

* Power outages
* Low battery conditions
* Low runtime warnings
* Connection failures
* Battery replacement recommendations

Notifications can be customized in the application settings.

---

## Does UPSLink work outside my home network?

UPSLink is designed primarily for local network monitoring.

Remote monitoring may be possible if your NUT server is securely exposed through VPN or other remote access solutions.

---

## What port does UPSLink use?

By default, NUT servers typically use:

```text
3493
```

Ensure the NUT server is reachable from your Android device.

---

## Can UPSLink monitor multiple UPS devices?

Yes.

UPSLink supports monitoring multiple UPS devices and multiple NUT server connections.

---

## Does UPSLink support Android widgets?

Yes.

UPSLink includes Android home screen widgets that can display UPS status information directly on your device.

---

## How do I connect UPSLink to Synology?

UPSLink can connect to Synology NAS devices using Synology's built-in Network UPS Server functionality.

### Configure Synology

1. Connect your UPS to the Synology NAS using USB.

2. Open DSM.

3. Navigate to:

   **Control Panel → Hardware & Power → UPS**

4. Enable:

   * **Enable UPS Support**
   * **Enable Network UPS Server**

5. Click **Permitted DiskStation Devices**.

6. Add the IP address of the Android device running UPSLink.

### Configure UPSLink

1. Open UPSLink.
2. Tap **Add Connection**.
3. Enter the IP address of your Synology NAS.
4. Leave the port as **3493** unless you have customized it.
5. Enter credentials if required.
6. Tap **Discover Devices**.

UPSLink should automatically discover and connect to the UPS exposed by Synology's Network UPS Server.

---

## UPSLink cannot discover my Synology UPS

If UPSLink cannot discover your UPS:

1. Verify **Enable Network UPS Server** is enabled in DSM.
2. Verify your Android device and Synology NAS are on the same network.
3. Verify the Android device IP address has been added to **Permitted DiskStation Devices**.
4. Confirm port **3493** is not blocked by a firewall.
5. Try manually adding the Synology NAS IP address in UPSLink instead of using discovery.

---

## Is my data sent to a cloud service?

No.

UPSLink is designed to communicate directly with user-configured NUT servers and does not intentionally transmit UPS monitoring data to third-party cloud services.

---

## Where can I get support?

For support, questions, or feedback:

**Email:** [reelmemories1987@gmail.com](mailto:reelmemories1987@gmail.com)

**Website:** https://reelmemories.github.io/upslink/
