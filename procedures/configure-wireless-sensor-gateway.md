# Configure a Wireless Sensor Gateway

## Document control

| Field | Details |
|---|---|
| Document type | Technical procedure sample |
| Audience | Field technicians, installers, support specialists |
| Skill level | Basic to intermediate |
| Estimated time | 20–30 minutes |
| Applies to | Generic wireless sensor gateway and cloud monitoring dashboard |
| Last updated | 2026-06-22 |

> **Portfolio note:** This is a fictional, vendor-neutral procedure sample. Product names, IP addresses, screenshots, and UI labels are generic.

## Overview

This procedure explains how to install, configure, and verify a wireless sensor gateway. The gateway receives readings from wireless sensors and sends the data to a cloud monitoring dashboard.

Use this procedure when setting up a new gateway at a customer site, replacing a failed gateway, or confirming that a gateway can communicate with a test sensor.

## Before you begin

Complete these checks before starting the setup.

### Required equipment

- Wireless sensor gateway
- Compatible wireless sensor
- Approved gateway power adapter
- Ethernet cable
- Laptop, tablet, or service phone
- Access to the customer network
- Monitoring dashboard account
- Gateway serial number
- Site name, customer ID, or work order number
- Small screwdriver, if the gateway uses a mounting bracket

### Network requirements

The gateway requires:

- Active internet connection
- DHCP-enabled router, unless the site uses a static IP address
- Outbound HTTPS traffic allowed on port `443`
- Gateway and technician device connected to the same local network during setup
- Sensor placed within the approved wireless range
- Gateway mounted away from large motors, compressors, metal panels, and high-voltage wiring when possible

### Account requirements

Before setup, confirm that you can sign in to the monitoring dashboard and that your account has permission to:

- Add a gateway
- Add or pair a sensor
- Assign devices to a customer site
- View live readings
- Clear setup alerts

## Safety and caution notes

> **Caution:** Use only the approved power adapter for the gateway. The wrong adapter may damage the device or create an electrical hazard.

> **Caution:** Do not mount the gateway inside a metal cabinet unless the site plan includes an external antenna. Metal can block wireless signals.

> **Caution:** Keep cables away from walkways, moving parts, hot surfaces, and sharp edges.

> **Notice:** Do not share customer Wi-Fi passwords, dashboard credentials, device serial numbers, or network details outside approved service channels.

> **Notice:** This sample does not replace product-specific installation instructions, electrical codes, or site safety rules.

## Setup diagram

![Gateway setup diagram](../assets/gateway-setup-diagram.svg)

## Procedure

### 1. Inspect the gateway

1. Remove the gateway from the package.
2. Confirm that the gateway serial number is readable.
3. Inspect the enclosure, antenna, ports, and power connector.
4. Check that the gateway model matches the work order.
5. Do not install the gateway if the case is cracked, the antenna is loose, or the ports are damaged.

### 2. Choose the gateway location

1. Select a location near an active network connection and power outlet.
2. Place the gateway above floor level when possible.
3. Keep the gateway away from large metal objects, compressors, motors, and high-voltage wiring.
4. Confirm that the location is dry and protected from direct spray.
5. Do not permanently mount the gateway until pairing and signal strength are verified.

### 3. Connect the gateway to the network

1. Connect one end of the Ethernet cable to the gateway LAN port.
2. Connect the other end to an active router, switch, or network jack.
3. Confirm that the Ethernet cable clicks into place.
4. Check the network LED.

Expected result: The network LED turns on or begins blinking after the gateway starts.

### 4. Connect power

1. Connect the approved power adapter to the gateway.
2. Plug the adapter into a grounded outlet.
3. Wait 60–90 seconds for the gateway to start.
4. Confirm that the power LED turns solid green.

Expected result: The gateway powers on and the startup sequence completes.

### 5. Open the gateway setup page

1. Connect your laptop, tablet, or service phone to the same local network as the gateway.
2. Open a web browser.
3. Enter the gateway setup address listed on the installation label, job ticket, or setup card.
4. Sign in with the temporary setup credentials.
5. Change the temporary password if prompted.

Expected result: The gateway setup page opens and shows the gateway status.

> **Tip:** If the setup page does not open, confirm that your service device is on the same local network as the gateway.

### 6. Register the gateway

1. Select **Gateway Setup**.
2. Enter the site name or customer ID.
3. Enter the gateway serial number.
4. Select the correct time zone.
5. Confirm the network settings.
6. Select **Save**.
7. Wait for the status message: **Gateway registered successfully**.

Expected result: The monitoring dashboard shows the gateway as **Online**.

### 7. Pair a test sensor

1. Place the sensor within 10 feet of the gateway.
2. In the gateway setup page, select **Add Device**.
3. Press the pairing button on the sensor.
4. Wait for the sensor ID to appear.
5. Select the sensor ID.
6. Enter a clear sensor name, such as `Walk-In Freezer Temp 01`.
7. Select the sensor type.
8. Select **Pair Device**.
9. Wait for the status message: **Device paired successfully**.

Expected result: The sensor appears in the device list with a paired status.

### 8. Move the sensor to the target location

1. Move the sensor to the planned installation location.
2. Keep the sensor away from direct water spray, moving parts, high-voltage wiring, and hot surfaces.
3. Mount the sensor according to the site plan.
4. Wait 2–5 minutes for the next reading.
5. Refresh the dashboard.

Expected result: The sensor sends a new reading from the target location.

### 9. Confirm signal strength

1. Open the sensor details page.
2. Check the signal strength value.
3. Confirm that the signal strength is **Fair**, **Good**, or **Excellent**.
4. If the signal strength is **Weak**, move the sensor or gateway and check again.

Expected result: The sensor has a stable signal before the technician leaves the site.

### 10. Record the installation details

Record the following details in the service notes:

- Gateway serial number
- Gateway location
- Sensor ID
- Sensor name
- Sensor location
- Signal strength
- Date and time of installation
- Any site-specific notes

## Verification steps

After setup, confirm each item below.

| Check | Expected result | Pass/Fail |
|---|---|---|
| Gateway power LED | Solid green |  |
| Gateway network LED | Blinking or solid green |  |
| Gateway dashboard status | Online |  |
| Gateway assigned to correct site | Correct site name or customer ID appears |  |
| Test sensor status | Paired |  |
| Sensor reading | Updated within the last 5 minutes |  |
| Sensor signal strength | Fair, Good, or Excellent |  |
| Alert state | No active setup alerts |  |
| Service notes | Serial number and sensor location recorded |  |

## Screenshot placeholders

Use these placeholder names if the repository is expanded with real screenshots later.

| Screenshot file | Purpose |
|---|---|
| `gateway-login.png` | Shows the gateway setup login page |
| `gateway-registration.png` | Shows the gateway registration form |
| `add-device.png` | Shows the Add Device screen |
| `sensor-online.png` | Shows a paired sensor with a live reading |
| `signal-strength.png` | Shows the sensor signal strength field |

## Troubleshooting

| Problem | Possible cause | Corrective action |
|---|---|---|
| Power LED does not turn on | Loose power adapter or failed outlet | Check the outlet, adapter, and gateway power port. Try a known-good outlet. |
| Network LED does not turn on | Bad Ethernet cable or inactive network jack | Try another Ethernet cable or network port. Confirm the switch or router has power. |
| Setup page does not open | Technician device is on a different network | Connect the technician device to the same local network as the gateway. |
| Setup page opens but login fails | Temporary password was changed or entered incorrectly | Confirm the setup credentials. Reset the gateway password only if approved by the service process. |
| Gateway does not register | Internet access is blocked | Confirm outbound HTTPS traffic on port `443` is allowed. Check firewall rules with the site contact. |
| Gateway shows offline in dashboard | Gateway has local network access but no cloud connection | Restart the gateway, check internet access, and confirm dashboard service availability. |
| Sensor does not appear during pairing | Sensor is asleep, out of range, or already paired | Wake the sensor, move it closer to the gateway, or reset pairing according to the device instructions. |
| Sensor pairs but does not report readings | Sensor has not sent its first reading yet | Wait for the reporting interval, refresh the dashboard, and check the sensor battery. |
| Sensor shows weak signal | Gateway is too far away or blocked by metal | Move the gateway or sensor to improve line of sight. Avoid metal cabinets and dense walls. |
| Wrong site appears in dashboard | Gateway was assigned to the wrong customer or location | Stop setup and contact support before adding more sensors. |

## Rollback steps

Use these steps if setup cannot be completed.

1. Record the error message shown in the gateway setup page or dashboard.
2. Capture a screenshot if allowed by the customer and service policy.
3. Unpair the test sensor if it was added to the wrong site.
4. Disconnect the gateway from power.
5. Label the gateway as **Setup incomplete**.
6. Escalate the issue with the gateway serial number, site name, and troubleshooting steps already performed.

## Escalation information to collect

Before contacting support, collect:

- Gateway serial number
- Gateway model
- Sensor ID
- Customer site name or ID
- Network type: Ethernet, Wi-Fi bridge, or cellular router
- LED status
- Error message text
- Time the issue occurred
- Steps already completed

## Completion criteria

The procedure is complete when:

- The gateway is online.
- At least one sensor is paired.
- A live sensor reading appears in the monitoring dashboard.
- Sensor signal strength is acceptable.
- No setup alerts are active.
- The technician records the gateway serial number and sensor location in the service notes.

## Related procedures

- [Troubleshoot Failed Device Pairing](troubleshoot-failed-device-pairing.md)
- [Run a System Health Check](run-system-health-check.md)

## Revision history

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-06-22 | Initial portfolio sample |
