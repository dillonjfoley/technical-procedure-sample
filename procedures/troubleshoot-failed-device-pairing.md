# Troubleshoot Failed Device Pairing

## Document control

| Field | Details |
|---|---|
| Document type | Technical troubleshooting procedure sample |
| Audience | Field technicians, installers, support specialists |
| Skill level | Basic to intermediate |
| Estimated time | 10–20 minutes |
| Applies to | Generic wireless sensors, gateways, and cloud monitoring dashboard |
| Related procedure | [Configure a Wireless Sensor Gateway](configure-wireless-sensor-gateway.md) |
| Last updated | 2026-06-22 |

> **Portfolio note:** This is a fictional, vendor-neutral procedure sample. Product names, device IDs, screenshots, and UI labels are generic.

## Overview

Use this procedure when a wireless sensor fails to pair with a gateway during setup, replacement, or service. Pairing can fail because of power, distance, wireless interference, duplicate registration, gateway connectivity, dashboard permissions, or a damaged device.

This procedure helps the technician isolate the failure point before replacing hardware or escalating to support.

## When to use this procedure

Use this procedure when one or more of the following symptoms occurs:

- The sensor does not appear in the **Add Device** screen.
- The sensor appears but pairing does not complete.
- The gateway shows a pairing timeout message.
- The sensor status stays **Offline**, **Pending**, or **Not Reporting**.
- The sensor pairs but does not send a reading.
- The dashboard shows that the sensor is already assigned to another site or gateway.
- The signal strength is weak after pairing.

## Before you begin

### Required equipment

- Wireless sensor gateway
- Wireless sensor that failed pairing
- Known-good sensor, if available
- Approved replacement battery, if the sensor uses a replaceable battery
- Laptop, tablet, or service phone
- Monitoring dashboard account
- Gateway serial number
- Sensor ID or QR code
- Site name, customer ID, or work order number

### Account requirements

Before troubleshooting, confirm that your dashboard account has permission to:

- View the customer site
- View gateway status
- Add or pair a device
- Remove or unassign a device, if allowed by the service process
- View device history
- View setup alerts

### Gateway requirements

Before troubleshooting the sensor, confirm that the gateway is ready for pairing.

| Gateway check | Expected result |
|---|---|
| Power status | Power LED is solid green |
| Network status | Network LED is blinking or solid green |
| Dashboard status | Gateway shows **Online** |
| Site assignment | Gateway is assigned to the correct site |
| Add Device screen | Technician can open the pairing screen |
| Recent communication | Gateway checked in within the last 5 minutes |

> **Tip:** If the gateway is offline, troubleshoot gateway connectivity before troubleshooting the sensor.

## Safety and caution notes

> **Caution:** Do not open a powered electrical cabinet unless you are trained and authorized to do so.

> **Caution:** Keep hands, tools, and sensor cables away from moving parts, fan blades, compressors, belts, hot surfaces, and high-voltage wiring.

> **Caution:** Do not install or move a sensor in a location that requires climbing, lifting, or reaching beyond approved site safety rules.

> **Notice:** Do not reset a gateway unless the service process allows it. A reset may remove active customer devices or interrupt monitoring.

> **Notice:** Do not share customer Wi-Fi passwords, dashboard credentials, serial numbers, or site details outside approved service channels.

> **Notice:** This sample does not replace product-specific service instructions, electrical codes, or site safety rules.

## Pairing workflow diagram

![Pairing workflow diagram](../assets/pairing-flow-diagram.svg)

## Quick checks

Start with these checks before replacing hardware.

| Check | Expected result | Action if failed |
|---|---|---|
| Gateway is powered | Power LED is solid green | Check outlet, power adapter, and gateway power port |
| Gateway is online | Dashboard shows **Online** | Restore network connection before pairing |
| Correct site is open | Site name or customer ID matches the work order | Switch to the correct site before pairing |
| Sensor battery is installed | Sensor LED flashes when awakened | Reseat or replace the battery |
| Sensor is close to gateway | Sensor is within 10 feet during pairing | Move sensor closer and retry |
| Sensor is awake | Sensor LED flashes after button press | Press the pairing button again or replace the battery |
| Sensor is not already assigned | Sensor ID is not listed under another site or gateway | Unassign it or escalate according to service policy |

## Troubleshooting procedure

### 1. Record the failure state

1. Open the **Add Device** or pairing screen.
2. Attempt to pair the sensor one time.
3. Record what happens.
4. Write down the exact error message, if shown.
5. Capture a screenshot if allowed by customer and service policy.

Expected result: You have a clear starting point before changing settings or replacing parts.

Record one of the following failure states:

- Sensor does not appear.
- Sensor appears but pairing times out.
- Sensor pairs but stays offline.
- Sensor pairs but does not report a reading.
- Sensor shows **Already Assigned**.
- Sensor shows weak signal after pairing.

### 2. Confirm the gateway is online

1. Open the monitoring dashboard.
2. Search for the gateway serial number.
3. Confirm that the gateway status is **Online**.
4. Confirm that the gateway is assigned to the correct customer site.
5. Check the gateway's last communication time.

Expected result: The gateway is online and has checked in within the last 5 minutes.

If the gateway is offline, stop this procedure and restore gateway connectivity before pairing the sensor.

### 3. Move the sensor closer to the gateway

1. Place the sensor within 10 feet of the gateway.
2. Keep the sensor and gateway in the same room if possible.
3. Remove metal objects between the sensor and gateway.
4. Keep the sensor away from compressors, motors, electrical panels, and high-voltage wiring.
5. Try pairing again.

Expected result: The sensor appears in the **Add Device** screen.

> **Tip:** Pair the sensor near the gateway first. After pairing succeeds, move the sensor to its final location and verify signal strength.

### 4. Wake the sensor

1. Press the sensor pairing button.
2. Watch the sensor LED.
3. Confirm that the LED flashes.
4. Wait up to 60 seconds for the sensor ID to appear in the dashboard.
5. If the sensor does not appear, press the pairing button one more time.

Expected result: The sensor LED flashes and the sensor ID appears in the dashboard.

If the LED does not flash, continue to the battery check.

### 5. Check the sensor battery

1. Remove the sensor battery cover if the model allows battery replacement.
2. Confirm that the battery is installed in the correct direction.
3. Check for corrosion, loose contacts, or damage.
4. Reseat the battery.
5. Replace the battery with an approved known-good battery if available.
6. Wake the sensor again.

Expected result: The sensor LED flashes after the battery is reseated or replaced.

> **Caution:** Use only the approved battery type for the sensor. The wrong battery may damage the sensor or create a safety risk.

### 6. Check for duplicate registration

1. In the dashboard, search for the sensor ID.
2. Confirm that the sensor is not assigned to another site.
3. Confirm that the sensor is not assigned to another gateway at the same site.
4. If the sensor is already assigned, follow the approved process to unassign or transfer the device.
5. Try pairing again after the duplicate record is cleared.

Expected result: The sensor is available for pairing with the correct gateway.

> **Notice:** Do not remove a sensor from an active customer site unless the work order or service lead approves the change.

### 7. Restart pairing mode

1. Exit the **Add Device** screen.
2. Wait 30 seconds.
3. Open **Add Device** again.
4. Press the sensor pairing button.
5. Select the sensor ID when it appears.
6. Select **Pair Device**.
7. Wait for the pairing confirmation message.

Expected result: The dashboard shows **Device paired successfully**.

### 8. Check the sensor reporting interval

Use this step if the sensor pairs but does not show a reading.

1. Open the sensor details page.
2. Check the last reading time.
3. Wait for one full reporting interval.
4. Refresh the dashboard.
5. Wake the sensor manually if the device supports manual reporting.
6. Confirm that a new reading appears.

Expected result: A new sensor reading appears in the dashboard.

> **Tip:** Some sensors do not report immediately after pairing. Wait for the expected reporting interval before replacing hardware.

### 9. Verify signal strength at the final location

1. Move the sensor to the planned installation location.
2. Wait 2–5 minutes for the next reading.
3. Refresh the sensor details page.
4. Check signal strength.
5. Confirm that the signal strength is **Fair**, **Good**, or **Excellent**.
6. If signal strength is **Weak**, move the sensor or gateway and check again.

Expected result: The sensor reports from the final location with acceptable signal strength.

### 10. Test with known-good hardware

Use this step only after completing the previous checks.

1. Pair a known-good sensor to the same gateway.
2. If the known-good sensor pairs, mark the original sensor as suspect.
3. If the known-good sensor does not pair, mark the gateway, dashboard settings, or network as suspect.
4. Record both test results in the service notes.

Expected result: Testing separates a sensor issue from a gateway, account, or network issue.

## Troubleshooting table

| Problem | Possible cause | Corrective action |
|---|---|---|
| Sensor does not appear in the Add Device screen | Sensor is asleep | Press the pairing button and wait up to 60 seconds |
| Sensor LED does not flash | Dead battery or loose battery contact | Reseat or replace the battery |
| Sensor appears, then disappears | Weak wireless signal | Move the sensor within 10 feet of the gateway and retry |
| Pairing times out | Gateway is busy or has unstable connectivity | Exit pairing mode, wait 30 seconds, confirm gateway online status, and retry |
| Sensor shows Already Assigned | Sensor is registered to another site or gateway | Search the sensor ID and follow the approved unassignment process |
| Sensor pairs but stays Offline | Sensor has not sent a post-pairing check-in | Wait for one reporting interval, wake the sensor, and refresh the dashboard |
| Sensor pairs but no reading appears | Reporting interval has not passed or sensor input is disconnected | Wait for the interval and check sensor wiring or probe connection if applicable |
| Sensor reports from nearby but not final location | Final location has poor wireless coverage | Move the sensor, move the gateway, or use an approved repeater if available |
| Signal strength is Weak | Metal, distance, walls, or equipment interference | Improve line of sight and avoid metal cabinets, motors, and electrical panels |
| Correct sensor ID appears under wrong site | Technician is viewing or using the wrong customer site | Stop setup, switch to the correct site, and confirm assignment before continuing |
| Multiple sensors appear during pairing | Nearby sensors are also in pairing mode | Confirm the sensor ID on the label or QR code before selecting a device |
| Known-good sensor also fails | Gateway, account, dashboard, or network issue | Escalate with gateway serial number, account permissions, and network status |

## Verification steps

After the corrective action, confirm each item below.

| Check | Expected result | Pass/Fail |
|---|---|---|
| Gateway dashboard status | Online |  |
| Gateway site assignment | Correct site name or customer ID appears |  |
| Sensor ID | Matches the label, QR code, or work order |  |
| Sensor pairing status | Paired, Online, or Reporting |  |
| Sensor reading | Updated within the expected reporting interval |  |
| Sensor signal strength | Fair, Good, or Excellent |  |
| Active setup alerts | No unresolved pairing alerts |  |
| Service notes | Corrective action is recorded |  |

## Rollback steps

Use these steps if pairing cannot be completed.

1. Record the final error message or failure state.
2. Capture a screenshot if allowed.
3. Remove any incorrect or partial device assignment if approved by service policy.
4. Return the sensor to its original state if possible.
5. Label the device as **Pairing incomplete** or **Suspect sensor**, according to local process.
6. Leave active customer devices unchanged.
7. Escalate with the required information below.

## Escalation information to collect

Before contacting support, collect:

- Gateway serial number
- Gateway model, if available
- Sensor ID
- Sensor model or sensor type
- Customer site name or ID
- Dashboard user role or permission level
- Gateway status and last check-in time
- Sensor LED behavior
- Error message text
- Screenshot of the failure, if allowed
- Distance between gateway and sensor during pairing
- Signal strength, if shown
- Battery replacement result
- Known-good sensor test result, if performed
- Steps already completed

## Completion criteria

The issue is resolved when:

- The sensor is paired to the correct gateway.
- The sensor is assigned to the correct customer site.
- The sensor status shows **Online**, **Paired**, or **Reporting**.
- A live sensor reading appears in the monitoring dashboard.
- Signal strength is acceptable at the final installation location.
- No unresolved pairing alerts remain.
- The technician records the corrective action in the service notes.

## Related procedures

- [Configure a Wireless Sensor Gateway](configure-wireless-sensor-gateway.md)
- [Run a System Health Check](run-system-health-check.md)
