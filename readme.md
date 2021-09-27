# Matter (CHIP) with nrf52840dk and Zephyr RTOS

- CHIP : ConnectedHomeIP : https://github.com/project-chip/connectedhomeip
- Nordic Semos : sdk-nrf : https://github.com/nrfconnect/sdk-nrf

## Samples :

- `light_switch` : https://github.com/nrfconnect/sdk-nrf/tree/master/samples/matter/light_switch
    - https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/samples/matter/light_switch/README.html
- `light_bulb` : https://github.com/nrfconnect/sdk-nrf/tree/master/samples/matter/light_bulb

Build using SEGGER

Click button 3 on both board after power up.

## Results :

![](/pics/coms.png)

## Todo

- Enable `matter` shell with `CONFIG_CHIP_LIB_SHELL=y`
    - https://github.com/project-chip/connectedhomeip/blob/master/docs/guides/nrfconnect_examples_cli.md#using-cli-in-nrf-connect-examples

- Compile on Linux without SEGGER :
```
export ZEPHYR_BASE=/home/lucas/zephyrproject/zephyr
export ZEPHYR_NRF_MODULE_DIR=/home/lucas/sdk-nrf
export ZEPHYR_CONNECTEDHOMEIP_MODULE_DIR=/home/lucas/connectedhomeip
export ZEPHYR_TOOLCHAIN_VARIANT=gnuarmemb
export GNUARMEMB_TOOLCHAIN_PATH="/usr/share/gcc-arm-none-eabi-10.3-2021.07

west build -p auto -b nrf52840dk_nrf52840 .
```

## Ressources : 

- [Matter (Project CHIP)](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/ug_matter.html#ug-matter)
- [nRF Connect SDK installation](https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/gs_assistant.html#gs-app-tcm)
    - [nRF Connect for VS Code](https://nordicplayground.github.io/vscode-nrf-connect/)
    - [CHIP nRF Connect Lighting Example Application](https://github.com/project-chip/connectedhomeip/tree/master/examples/lighting-app/nrfconnect)

## Other

- Zephyr : 
    - On Linux, without nRF Connect : 
        - https://docs.zephyrproject.org/latest/getting_started/toolchain_3rd_party_x_compilers.html
        - https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm
            - https://howtoinstall.co/en/gcc-arm-none-eabi?action=uninstall
            - https://docs.zephyrproject.org/latest/getting_started/index.html
    - https://docs.zephyrproject.org/latest/guides/modules.html#modules
    - https://docs.zephyrproject.org/latest/application/index.html#env-vars
    - https://docs.zephyrproject.org/latest/getting_started/index.html