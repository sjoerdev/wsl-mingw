# mingw-w64 wsl2 template

This is a way to do windows development using a wsl enviroment and linux tools.

## requirements:

1. make sure you have wsl2 with `build-essential` installed

2. install mingw-w64 (ucrt) on debian: `sudo apt install g++-mingw-w64-ucrt64 gcc-mingw-w64-ucrt64`

3. enable wsl interop, add `enabled = true` and `appendWindowsPath = true` under `[interop]` inside `/etc/wsl.conf`

4. restart wsl after enabling interop manually via powershell `wsl --shutdown`

5. make sure interop is enabled: `ls /proc/sys/fs/binfmt_misc/` should contain `WSLInterop`