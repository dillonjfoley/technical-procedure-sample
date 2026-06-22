# Run a System Health Check

## Document control

| Field | Details |
|---|---|
| Document type | Technical procedure sample |
| Audience | Field technicians, installers, support specialists |
| Skill level | Basic to intermediate |
| Estimated time | 10–15 minutes |
| Applies to | Generic wireless sensor gateway, wireless sensors, and cloud monitoring dashboard |
| Related procedures | [Configure a Wireless Sensor Gateway](configure-wireless-sensor-gateway.md), [Troubleshoot Failed Device Pairing](troubleshoot-failed-device-pairing.md) |
| Last updated | 2026-06-22 |

> **Portfolio note:** This is a fictional, vendor-neutral procedure sample. Product names, device IDs, IP addresses, screenshots, and UI labels are generic.

## Overview

Use this procedure to confirm that a wireless sensor gateway, paired sensors, and the monitoring dashboard are working correctly after installation, service, relocation, or troubleshooting.

A system health check verifies that:

- The gateway is powered and online.
- The gateway has recently checked in with the cloud dashboard.
- Expected sensors are paired and reporting.
- Sensor readings are current.
- Signal strength is acceptable.
- No setup-related alerts remain active.
- Service notes include enough detail for future support.

## When to use this procedure

Run this procedure:

- After configuring a new gateway.
- After pairing or replacing a sensor.
- After moving a gateway or sensor.
- After resolving a network issue.
- Before closing a service ticket.
- When a customer reports missing readings, offline devices, or repeated alerts.

## Before you begin

### Required equipment

- Laptop, tablet, or service phone
- Monitoring dashboard account
- Customer site name, gateway serial number, or work order number
- List of expected sensors for the site
- Access to the installed gateway and sensors, if physical checks are needed
- Approved replacement battery, if sensors use replaceable batteries
- Ethernet cable, if gateway network troubleshooting is needed

### Account requirements

Confirm that your dashboard account can:

- View the customer site
- View gateway status
- View device details
- View alerts or alarm history
- Acknowledge setup-related test alerts, if allowed
- Add service notes or update the work order

### Information to collect

Before starting, collect or confirm:

- Customer site name or customer ID
- Gateway serial number
- Gateway location
- Expected sensor count
- Expected sensor names or IDs
- Expected reporting interval
- Any open service ticket or work order number

## Safety and caution notes

> **Caution:** Follow site safety rules before entering equipment rooms, rooftops, machine rooms, refrigerated spaces, or areas near moving equipment.

> **Caution:** Do not touch exposed wiring, electrical panels, rotating equipment, compressors, or hot surfaces while checking gateway or sensor locations.

> **Caution:** Do not climb, reach above shoulder height, or enter restricted areas unless you are trained and authorized to do so.

> **Notice:** Do not reset a gateway, remove a sensor, clear an alert, or change dashboard settings unless the work order or service process allows it.

> **Notice:** Do not share customer Wi-Fi passwords, dashboard credentials, serial numbers, screenshots, or network details outside approved service channels.

> **Notice:** This sample does not replace product-specific service instructions, electrical codes, or site safety rules.

## Health check summary

| System area | What to check | Acceptable result |
|---|---|---|
| Gateway power | Power LED and dashboard status | Gateway is powered and shows **Online** |
| Gateway communication | Last check-in time | Gateway checked in within the expected interval |
| Sensor inventory | Device list | All expected sensors appear |
| Sensor communication | Last reading time | Each sensor reported within the expected interval |
| Sensor signal | Signal strength value | Signal is **Fair**, **Good**, or **Excellent** |
| Alerts | Active alerts page | No unresolved setup-related alerts |
| Documentation | Service notes | Exceptions and final status are recorded |

## Procedure

### 1. Open the customer site

1. Sign in to the monitoring dashboard.
2. Search for the customer site name, customer ID, or gateway serial number.
3. Open the correct customer site.
4. Confirm that the site name matches the work order.
5. Confirm that the gateway serial number matches the installed gateway.

Expected result: The correct customer site is open and the gateway serial number matches the work order.

> **Notice:** If the site name or gateway serial number does not match the work order, stop and confirm the correct site before making changes.

### 2. Confirm gateway power

1. Locate the installed gateway.
2. Check the power connection.
3. Confirm that the power adapter is plugged into the gateway and outlet.
4. Check the gateway power LED.
5. Record the LED state in the service notes.

Expected result: The gateway power LED is solid green or shows the approved normal power state for the device.

If the power LED is off, check the outlet, power adapter, and gateway power port before continuing.

### 3. Confirm gateway network connection

1. Check the gateway network LED.
2. Confirm that the Ethernet cable is fully seated, if the gateway uses Ethernet.
3. Confirm that the router, switch, or network jack has power.
4. In the dashboard, open the gateway details page.
5. Confirm that the gateway status shows **Online**.
6. Check the gateway's last check-in time.

Expected result: The gateway shows **Online** and has checked in within the expected interval.

> **Tip:** A blinking network LED usually means network activity. A dark network LED may indicate a loose cable, inactive port, or failed network device.

### 4. Review gateway details

1. On the gateway details page, confirm the gateway name.
2. Confirm the gateway location.
3. Confirm the assigned customer site.
4. Confirm the time zone.
5. Check for gateway-level warning messages.
6. Record any warning messages in the service notes.

Expected result: Gateway details match the site plan and no gateway-level setup warnings are active.

### 5. Confirm the expected sensor list

1. Open the device list for the site.
2. Compare the device list to the work order or site plan.
3. Confirm that each expected sensor appears.
4. Confirm that each sensor has a clear name, such as `Walk-In Cooler Temp 01`.
5. Confirm that each sensor is assigned to the correct gateway.
6. Record any missing, duplicate, or unclear sensor names.

Expected result: All expected sensors appear once and are assigned to the correct gateway.

If a sensor is missing, use [Troubleshoot Failed Device Pairing](troubleshoot-failed-device-pairing.md).

### 6. Check latest sensor readings

1. Open the first sensor details page.
2. Check the latest reading value.
3. Check the last reading time.
4. Confirm that the reading updated within the expected reporting interval.
5. Repeat these checks for each sensor at the site.
6. Record any stale, missing, or unusual readings.

Expected result: Each sensor has a current reading.

Use the table below to classify the reading status.

| Reading status | Meaning | Technician action |
|---|---|---|
| Current | Reading updated within the expected interval | Continue health check |
| Stale | Reading did not update within the expected interval | Check signal strength, battery, and gateway status |
| Missing | No reading appears after pairing | Confirm sensor type, battery, and pairing status |
| Unusual | Reading appears outside expected site conditions | Check sensor placement and compare with nearby conditions |

> **Tip:** Some sensors report on a schedule. Wait for one full reporting interval before marking a sensor as failed.

### 7. Check signal strength

1. Open each sensor details page.
2. Check the signal strength value.
3. Confirm that the signal strength is **Fair**, **Good**, or **Excellent**.
4. Record any sensor with **Weak** signal.
5. If signal is weak, inspect the sensor location.
6. Move the sensor or gateway only if the work order allows it.
7. Wait for the next reading after making any location change.

Expected result: Each sensor has stable signal strength before the service ticket is closed.

Common causes of weak signal include:

- Sensor mounted too far from the gateway
- Metal walls, metal shelving, or walk-in cooler panels between the sensor and gateway
- Gateway mounted inside a metal cabinet
- Interference from motors, compressors, electrical panels, or high-voltage wiring
- Low sensor battery

### 8. Review active alerts

1. Open the **Alerts** page.
2. Filter alerts by the customer site, if needed.
3. Review all active gateway, sensor, and setup-related alerts.
4. Confirm whether each alert is new, expected, or already known.
5. Acknowledge test alerts only if the service process allows it.
6. Record unresolved alerts in the service notes.

Expected result: No unresolved setup-related alerts remain after installation or service.

> **Notice:** Do not clear a customer-impacting alert just to close the service ticket. Document it and escalate according to the service process.

### 9. Check alert history

1. Open the alert history or event log.
2. Review events from the installation or service window.
3. Look for repeated offline, low battery, pairing, or weak signal events.
4. Confirm that any test alerts are documented.
5. Record repeated events that may require follow-up.

Expected result: The event history does not show repeated failures after the gateway and sensors are verified.

### 10. Perform a physical placement check

Use this step if readings are stale, signal is weak, or the customer reported intermittent issues.

1. Inspect the gateway location.
2. Confirm that the gateway is not inside a metal cabinet unless an approved external antenna is used.
3. Confirm that cables are secure and not stretched, pinched, or routed across walkways.
4. Inspect each sensor location.
5. Confirm that sensors are not blocked by metal objects or mounted near high-heat, high-moisture, or high-vibration areas unless approved for that environment.
6. Confirm that sensors are mounted securely.

Expected result: The gateway and sensors are installed in locations that support stable communication and safe operation.

### 11. Run a final dashboard refresh

1. Refresh the customer site dashboard.
2. Confirm the gateway still shows **Online**.
3. Confirm that all expected sensors still appear.
4. Confirm that readings and signal strength remain acceptable.
5. Confirm that no new setup-related alerts appeared during the health check.

Expected result: The dashboard shows a stable system after the final refresh.

### 12. Record service notes

Add the following details to the work order or service notes:

- Date and time of health check
- Technician name or initials
- Customer site name or customer ID
- Gateway serial number
- Gateway location
- Gateway online/offline status
- Last gateway check-in time
- Number of expected sensors
- Number of reporting sensors
- Sensors with weak signal, stale readings, or active alerts
- Corrective actions taken
- Open issues or escalation details

Expected result: The service record clearly explains the final system state.

## Verification checklist

Complete this checklist before closing the work order.

| Check | Expected result | Pass/Fail | Notes |
|---|---|---|---|
| Correct customer site opened | Site name or customer ID matches work order |  |  |
| Gateway serial number verified | Serial number matches installed gateway |  |  |
| Gateway power verified | Power LED shows normal state |  |  |
| Gateway online | Dashboard status shows **Online** |  |  |
| Gateway last check-in verified | Last check-in is within expected interval |  |  |
| Sensor list reviewed | All expected sensors appear |  |  |
| Sensor names reviewed | Sensor names are clear and location-based |  |  |
| Sensor readings reviewed | Readings are current |  |  |
| Signal strength reviewed | Signal is **Fair**, **Good**, or **Excellent** |  |  |
| Alerts reviewed | No unresolved setup-related alerts |  |  |
| Event history reviewed | No repeated failures after service |  |  |
| Physical placement checked | Gateway and sensors are safely placed |  |  |
| Service notes completed | Final status and exceptions are documented |  |  |

## Screenshot placeholders

Use these placeholder names if the repository is expanded with real screenshots later.

| Screenshot file | Purpose |
|---|---|
| `site-dashboard-health.png` | Shows the customer site dashboard with gateway and sensor status |
| `gateway-details-online.png` | Shows gateway online status and last check-in time |
| `sensor-list-current.png` | Shows sensors with current readings |
| `sensor-signal-strength.png` | Shows sensor signal strength values |
| `active-alerts-clear.png` | Shows no unresolved setup-related alerts |
| `service-notes-example.png` | Shows the type of information to record before closing the work order |

## Troubleshooting

| Problem | Possible cause | Corrective action |
|---|---|---|
| Gateway shows **Offline** | Gateway lost power or network access | Check the power adapter, outlet, Ethernet cable, router, switch, and network jack. |
| Gateway has power but no network LED | Loose Ethernet cable or inactive network port | Reseat the cable, try a known-good cable, or test another network port. |
| Gateway last check-in is old | Internet access is blocked or gateway cannot reach cloud service | Confirm local internet access and verify that outbound HTTPS traffic on port `443` is allowed. |
| Sensor is missing from the device list | Sensor was not paired or was assigned to another site | Search for the sensor ID and follow the pairing troubleshooting procedure. |
| Sensor reading is stale | Sensor is asleep, out of range, or battery is low | Wake the sensor, check signal strength, and replace the battery if approved. |
| Sensor reading appears incorrect | Sensor is mounted in the wrong location or affected by nearby heat/cold source | Compare the sensor location to the site plan and reposition if approved. |
| Sensor signal is weak | Distance, metal obstruction, or interference | Move the sensor closer to the gateway, move the gateway, or remove obstructions if possible. |
| Setup alert remains active | Alert was triggered during installation testing | Confirm the alert condition is resolved, then acknowledge only if allowed by service policy. |
| Repeated offline events appear in history | Intermittent power, network, or signal issue | Check cable strain, outlet stability, network equipment, and gateway placement. |
| Dashboard does not show recent changes | Browser cache or dashboard refresh delay | Refresh the page, sign out and back in, or wait one reporting interval. |

## Rollback or recovery steps

Use these steps only if a change made during the health check causes a problem.

1. Return the gateway or sensor to its previous approved location, if it was moved.
2. Restore the previous dashboard setting, if a setting was changed.
3. Reconnect any cable that was disconnected during inspection.
4. Wait for one reporting interval.
5. Refresh the dashboard and confirm the system status.
6. Document the rollback action in the service notes.

> **Notice:** Do not factory reset the gateway or remove customer devices as a rollback step unless the service process specifically approves it.

## Escalation criteria

Escalate the issue if any of the following conditions remain after troubleshooting:

- Gateway remains offline after power and network checks.
- Gateway serial number does not match the customer site.
- Multiple sensors stop reporting at the same time.
- A sensor has current power but will not report after battery and signal checks.
- Repeated offline or weak signal events continue after relocation.
- Dashboard permissions prevent the technician from viewing or confirming system status.
- Customer-impacting alerts remain active after service.
- The technician finds damaged hardware, exposed wiring, or an unsafe installation location.

When escalating, include:

- Customer site name or customer ID
- Gateway serial number
- Sensor IDs involved
- Error messages or alert names
- Last successful check-in time
- Steps already completed
- Screenshots, if allowed by policy
- Any site safety concerns

## Completion criteria

The system health check is complete when:

- The correct customer site has been verified.
- The gateway shows **Online**.
- The gateway has checked in within the expected interval.
- All expected sensors appear in the dashboard.
- Sensor readings are current or exceptions are documented.
- Signal strength is acceptable or exceptions are documented.
- No unresolved setup-related alerts remain.
- Service notes include final status, corrective actions, and open issues.

If any completion item fails, do not close the work order until the issue is corrected, documented as an approved exception, or escalated.

## Related procedures

- [Configure a Wireless Sensor Gateway](configure-wireless-sensor-gateway.md)
- [Troubleshoot Failed Device Pairing](troubleshoot-failed-device-pairing.md)
