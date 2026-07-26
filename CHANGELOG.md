# Changelog

## [2.26.0](https://github.com/g4bri3lDev/OpenDisplay_Firmware/compare/Firmware-2.25.1...Firmware-2.26.0) (2026-07-26)


### Features

* quarter-tone musical buzzer with hardware PWM + non-blocking playback ([#98](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/98)) ([5ed21a9](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/5ed21a918d9aaa6c3fb4418391de65204d5b2b2b))
* wake on button press from deep sleep + 0x0052 duration payload ([#97](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/97)) ([d974f9d](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/d974f9d6740d7fac722e4f86855999096804efaa))
* **wifi/lan:** WiFi/LAN transport + tinfl inflate; pin pioarduino 55.03.39 ([#124](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/124)) ([2e2131b](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/2e2131b9980c9a46f1c8e56ce2d3dcb4b7aa5bd3))


### Bug Fixes

* **buttons:** prime ADC channel before setting ladder pin attenuation ([#125](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/125)) ([5202d58](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/5202d58c08fa766ae45943b19b2b2b15c8d958e6))
* **c6:** pin pioarduino and force-link os_mempool object ([0d95b37](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/0d95b37f04c377a442483a92fe87d7904abb5eab))
* **ci:** grant the release-please build job contents:write ([c12ed15](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/c12ed15d2efe826fedc488c0fc64d3dd257a88c9))
* **ci:** pass BUILD_VERSION as string to avoid float formatting issue ([#12](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/12)) ([779f21b](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/779f21b048147eef1b6bb0fb1f7109291834a453))
* **device_cli:** emit yamllint-clean YAML from dump_yaml ([#102](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/102)) ([c9d36d9](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/c9d36d92127d4c13e11a0dfb6339bdb2e3653675))
* **esp32:** deinit BLE before esp_restart() to stop reboot boot-loop ([#114](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/114)) ([cbdf2b2](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/cbdf2b2dafe8aa5aa3a9f8d2ead1a69bda301fbe))
* **esp32:** drain response ring between config-read chunks (audit S5) ([#113](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/113)) ([f29eab2](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/f29eab2242d1d2770233a889fe9a1fe9e26941d5))
* gate deep sleep on a quiet window instead of a single idle pass ([#94](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/94)) ([ee98b65](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/ee98b6591273c828213bb7f13f6a8ba504f9b065))
* move WiFi handling after BLE command queue processing ([#30](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/30)) ([47fe7ce](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/47fe7ce40bb51a7a8f0bd1bfb79397817ff65397))
* **nrf:** guard Wire.begin() behind I2C bus config check ([#99](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/99)) ([cc0d752](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/cc0d7520ea0667115baf0226e1bbe9cccbfa6391))
* re-init I2C bus before AXP2101 probe in initAXP2101 ([#81](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/81)) ([975f14a](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/975f14a81d64acff7ca75cf16e5937760f9cadac)), closes [#37](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/37)
* validate config CRC with CRC-16/CCITT (advisory) to match toolbox/nRF/Silabs ([#83](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/83)) ([ff3656f](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/ff3656f6dca6ac4e666b0140df2b4ebb48eefb75))
* write both bitplanes for BWR/BWY direct display ([#82](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/82)) ([942018e](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/942018e1356f61526c7466eaa16c89bc0b74c9ef))


### Performance Improvements

* **esp32:** reuse mbedtls CCM context across session instead of per-packet ([#118](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/118)) ([67a83d3](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/67a83d38711f4d7a78645dc585546ad1526ed365))
* reclaim ~10.7 KB RAM — BLE GATT ceiling + config de-double-buffering ([#123](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/123)) ([29dc9da](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/29dc9daf44121d15b603a59956a4d6091c43fdcf))


### Code Refactoring

* **comm:** centralize + declutter command/response serial logging ([#115](https://github.com/g4bri3lDev/OpenDisplay_Firmware/issues/115)) ([d7edee2](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/d7edee21384f256d89172a7abf345cc7c3a595d0))


### Continuous Integration

* add Discord release notifications ([06bd44c](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/06bd44c10f4a4788d5e27d79f428966d25d08b4b))
* adopt release-please for firmware releases ([056f779](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/056f779c5cc6a0d21f41b7c2bcd9bbd85fad3d84))
* build release targets from a shared matrix manifest ([d3ce8bb](https://github.com/g4bri3lDev/OpenDisplay_Firmware/commit/d3ce8bbc03570e545edf023c72f98b4cfc9599ad))
