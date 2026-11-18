# Steady Node firmware updates

## Test: 0.1.99 → 0.1.100

The connected test board is running **0.1.99** with the simplified firmware interface. **0.1.100** is available here to test the full update flow.

1. Refresh the device dashboard: the Firmware button in Support shows a red **1**.
2. Open Firmware: the available version and **Update Steady Node** button are ready.
3. Confirm once. Progress shows downloading, transfer, installation and restart.
4. The device returns to the main page with a success message after the expected firmware responds.

Current version, **Check for updates**, and local-file installation remain available. The server address and Last check are not shown in the device interface.

Stable manifest: https://micromarty.github.io/SN_2U_UpDate/latest.json

[0.1.100 local upload package](https://micromarty.github.io/SN_2U_UpDate/releases/0.1.100/SteadyNode-V2-0.1.100.snp)

These builds are exclusively for ROM DFU board `2073389B4B30`, USB runtime `42003B001650304B59383820`, signed by its existing approved board key. Production trust is unchanged. Baseline 0.1.99 was physically verified; the 0.1.100 candidate is compiled and signed for the owner to test. Both sources differ only in version numbers.

See releases/0.1.100/release.json for hashes and validation details. Only public firmware artifacts and metadata are published; no source, private signing keys or provisioning images.
