# LineageOS Build Script Generator

This repository provides a **GitHub Actions workflow** to automatically generate a build script for **LineageOS**. The generated script is customized based on your input, allowing you to specify the Android version, device codename, device tree, vendor tree, and kernel tree.

The script is then published as a downloadable file in the **Releases** section of the repository.

## Features

- **Generate a customized LineageOS build script** for any device.
- Supports **Android version** customization (e.g., LineageOS 21, LineageOS 20, etc.).
- Supports **device tree**, **kernel**, and **vendor tree** from **GitHub repositories**.
- Automatically installs necessary dependencies for **Linux** and **Termux**.
- The generated script can be executed on your local machine or in a CI/CD environment.

## Prerequisites

- A GitHub account.
- Basic understanding of **Android** custom ROMs and **LineageOS**.
- Access to the **device tree**, **vendor tree**, and **kernel tree** for your device.

## Setup Instructions

### 1. Fork this Repository

- Fork this repository to your GitHub account to enable modifications and triggering of the workflow.

### 2. Trigger the GitHub Actions Workflow

- Navigate to the **Actions** tab in the GitHub repository.
- Select the **Generate and Publish LineageOS Build Script** workflow.
- Click on **Run workflow** to trigger the workflow.

### 3. Input the Required Information

When prompted, provide the following inputs:

1. **Android version**:  
   The Android version for LineageOS (e.g., `21.0` for LineageOS 21).
   
2. **Device codename**:  
   The codename of your device (e.g., `a22x`, `ginkgo`, etc.).

3. **Device tree**:  
   Provide the URL of your device's tree (e.g., `https://github.com/yourusername/device_samsung_a22x`).

4. **Vendor tree**:  
   Provide the URL of the vendor tree repository (e.g., `https://github.com/yourusername/vendor_samsung_a22x`).

5. **Kernel tree**:  
   Provide the URL of your device's kernel repository (e.g., `https://github.com/yourusername/android_kernel_samsung_a226b`).

6. **Release tag**:  
   Provide a tag name for the release (e.g., `v1.0`).

7. **Release name**:  
   Provide a name for the release (e.g., `LineageOS Build Script`).

### 4. Download the Build Script

After the workflow runs successfully:

- Navigate to the **Releases** section of the repository.
- Download the `build_lineage.sh` script from the **latest release**.

### 5. Run the Build Script

Once you have downloaded the `build_lineage.sh` script, follow these steps:

#### For Linux:

1. Make the script executable:

   ```bash
   chmod +x build_lineage.sh
   ```

2. Run the script:

   ```bash
   ./build_lineage.sh
   ```

#### For Termux (Android):

1. Make the script executable:

   ```bash
   chmod +x build_lineage.sh
   ```

2. Run the script:

   ```bash
   ./build_lineage.sh
   ```

---

## Script Details

- The script automatically installs required dependencies based on whether it's running on **Linux** or **Termux**.
- It initializes the **repo** tool, syncs the source code, and clones the device tree, vendor tree, and kernel tree from the provided URLs.
- It then builds LineageOS for your specified device.

## Contributing

Feel free to fork the repository, make modifications, and submit pull requests. If you encounter issues or need additional features, open an issue in the repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
