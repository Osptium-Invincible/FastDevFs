# Running Guide (for developers)
*We will keep updating this file with the latest detailed instructions as the project grows.*
## Install the FastDevFS
To install FastDevFS, follow these steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/devlup-labs/FastDevFs.git
   cd FastDevFs
   ```
2. Ensure you have the necessary dependencies installed, including FUSE3 and a C++ compiler.
    ``` bash
    sudo apt-get install libfuse3-dev g++
    ```
3. Build the project using CMake:
    ```bash
    mkdir -p build
    cd build
    cmake ..
    make
    ```

4. Run the filesystem (requires root privileges):
    ```bash
    mkdir -p ../test_mount_dir
    ./FastDevFS ../test_mount_dir -f ## Run in foreground mode
    ```
