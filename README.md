# mingw-w64 wsl2 template

This is a way to do windows development using a wsl enviroment and linux tools.

## requirements:

1. make sure you have wsl2 with `build-essential` installed

2. install mingw-w64 (ucrt) on debian: `sudo apt install g++-mingw-w64-ucrt64 gcc-mingw-w64-ucrt64`

3. open wsl config: `sudo nano /etc/wsl.conf`, and add this:
```
[interop]
enabled = true
appendWindowsPath = true
```

4. restart wsl manually via powershell `wsl --shutdown`
5. make sure interop is enabled: `ls /proc/sys/fs/binfmt_misc/` should contain `WSLInterop`