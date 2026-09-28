esp_dongle.bin固件

烧录参考命令
esptool.py --chip esp32s3 \
        -p /dev/ttyACM0 \
        -b 460800 \
        --before=default_reset \
        --after=hard_reset \
        write_flash \
        --flash_mode dio \
        --flash_freq 80m \
        --flash_size 4MB \
        0x0 esp_dongle.bin


测试方法：
WiFi 连接 ESP-Wireless-Disk，无密码
登录192.168.4.1，即可管理SD卡中的内容，可以下载里面的文件，或者删除等。