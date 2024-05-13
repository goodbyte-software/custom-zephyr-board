# Custom Zephyr Board

This repository demonstrates how to define and use a custom board configuration for the Zephyr Project, specifically using the [nRF52 DK](https://www.nordicsemi.com/Products/Development-hardware/nRF52-DK) as the base hardware.

## Prerequisites

To use this repository, you must have the following tools installed:
- `arm-none-eabi-gcc`: GCC toolchain for ARM processors.
- `west`: Zephyr’s meta-tool for building and managing multi-repository projects.
- `JLink`: Software for JTAG/SWD debugging and programming.
- `nrfjprog`: Utility for programming through SEGGER J-Link debuggers.

## Getting Started

1. **Clone the repository**:
    Begin by cloning this repository to your local machine.

2. **Initialize the workspace**:
    Use `west` to set up your Zephyr workspace:
    ```bash
    west init -l app && west update
    ```

3. **Build the application**:
    Compile your application for the custom board:
    ```bash
    west build -b goodbyte_demo app --pristine
    ```

4. **Flash the firmware** (Optional):
    If you're using the nRF52 DK, you can flash the built firmware directly onto the board:
    ```bash
    west flash
    ```

## Support

If you encounter any issues or have questions regarding the setup, please file an issue in this repository's Issue Tracker.

## Contributing

Contributions are welcome! If you'd like to improve the custom board definition or provide additional examples, please submit a pull request.
