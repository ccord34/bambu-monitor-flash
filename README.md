# Bambu Monitor 在线烧录

这是 Bambu Monitor for ESP32-S3 DualEye 的在线烧录页面仓库。

访问 GitHub Pages 后，使用桌面版 Chrome 或 Edge，通过 USB 数据线连接设备并点击页面中的“安装所选固件”即可刷写。

页面使用与本地 PlatformIO 成功验证一致的分段写入方式：

```text
0x0000  firmware/bootloader.bin
0x8000  firmware/partitions.bin
0xe000  firmware/boot_app0.bin
0x10000 firmware/firmware.bin
```

## 许可证

本仓库中的在线烧录页面和固件二进制仅允许个人、评估、维修和非商业部署使用。

不允许商用，包括但不限于：

- 销售预刷固件设备；
- 与收费产品捆绑；
- 提供收费刷机服务；
- 未经授权再分发获利；
- 将本固件作为商业方案的一部分使用。

详见 [LICENSE](LICENSE)。

## 离线刷写

如果不想使用网页在线烧录，可以下载离线刷写包：

[BambuMonitor-ESP32S3-DualEye-20260629-mapping-speed.zip](downloads/BambuMonitor-ESP32S3-DualEye-20260629-mapping-speed.zip)

解压后：

```powershell
.\flash.ps1 -Port COM13
```

或在 cmd 中：

```bat
flash.bat COM13
```

离线刷写包同样只允许个人、评估、维修和非商业部署使用，不允许商用。


