# Network Connection Troubleshooting

## Scenario

A user reports that their computer cannot connect to the internet.

## Initial Questions

Before making changes, I would establish:

- Is the issue affecting only this user or multiple users?
- Is the device connected through Wi-Fi or Ethernet?
- When did the problem start?
- Is there an error message?
- Can the user access any websites or internal systems?
- Did anything change before the issue occurred?

## Initial Checks

1. Check whether Wi-Fi or Ethernet is connected.
2. Check whether Airplane Mode is enabled.
3. Check whether other devices can connect to the same network.
4. Restart the network connection if appropriate.
5. Restart the computer if appropriate.
6. Check the device's network settings.

## Technical Checks

If the basic checks do not resolve the issue, I would investigate further using appropriate Windows networking tools.

Examples include:

- `ipconfig`
- `ping`
- `nslookup`

These can help identify whether the device has an IP address, whether it can communicate with another device, and whether DNS resolution is working.

## Example Commands

### Check IP configuration

```cmd
ipconfig


```markdown
!![Ping connectivity test](../screenshots/ping.png)

