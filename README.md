# Building C/C++ Barcode Reader with CMake

Version 6.3

## License
Get the [trial license](https://www.dynamsoft.com/CustomerPortal/Portal/Triallicense.aspx).

## Contact Us
https://www.dynamsoft.com/Company/Contact.aspx

## Windows
### Installation
* [Visual Studio Community](https://www.visualstudio.com/downloads/)
* [cmake-3.9.5-win64-x64.msi](https://cmake.org/files/v3.9/cmake-3.9.5-win64-x64.msi)
* [Dynamsoft Barcode Reader](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-Download.aspx).

### Steps
1. Copy **DBRx86.lib/DBRx64.lib** and **DynamsoftBarcodeReaderx86.dll/DynamsoftBarcodeReaderx64.dll** to **platforms\win** folder.
2. Create a **build** folder:
    ```
    mkdir build
    cd build
    ```
3. Edit **CMakeLists.txt** to replace the installation path with yours:
    ```
    set(CMAKE_INSTALL_PREFIX "e:/${PROJECT_NAME}")
    ```
4. Generate project configuration files for win32:
    ```bash
    cmake ..
    ```

    For win64:
    ```bash
    cmake -G"Visual Studio 14 2015 Win64" ..
    ```
5. Build and install the project:
    ```
    cmake --build . --target install
    ```
6. Run the app:
    ```
    cd e:\BarcodeReader\bin
    BarcodeReader.exe [barcode image file]
    ```

### Screenshot

![build barcode reader with cmake](images/screenshot.PNG)

## Linux 
1. Install **CMake**:
    ```bash
    sudo apt-get install cmake
    ```
2. Download [Dynamsoft Barcode Reader for Linux](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-for-Linux-Download.aspx). Copy **libDynamsoftBarcodeReader.so** to **platforms\linux**.
3. Create a **build** folder:
    ```
    mkdir build
    cd build
    ```
4. Build and install the project:
    ```bash
    sudo cmake --build . --target install
    ```
5. Run the app:
    ```
    BarcodeReader [barcode image file]
    ```

## macOS
1. Install **CMake**:
    ```bash
    brew install cmake
    ```
2. Download [Dynamsoft Barcode Reader for macOS](https://www.dynamsoft.com/Downloads/Dynamic-Barcode-Reader-Download.aspx?edition=macos&version=5.2). Copy **libDynamsoftBarcodeReader.dylib** to **platforms\macos**.
3. Create a **build** folder:
    ```
    mkdir build
    cd build
    ```
4. Build and install the project:
    ```bash
    cmake --build . --target install
    ```
5. Run the app:
    ```
    BarcodeReader [barcode image file]
    ```

## Reference
* https://cmake.org/cmake-tutorial/
* https://cmake.org/Wiki/CMake_Useful_Variables
* https://stackoverflow.com/questions/10671916/how-to-copy-dll-files-into-the-same-folder-as-the-executable-using-cmake
* https://cmake.org/Wiki/CMake_RPATH_handling

## Blog
* [CMake: Build C++ Project for Windows, Linux and macOS](http://www.codepool.biz/cmake-cc-windows-linux-macos.html)
* [My First C/C++ App Built with CMake on Windows](http://www.codepool.biz/cc-barcode-app-cmake-windows.html)
