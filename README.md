# RTMP_ffmpeg

> 该项目运行前需要配置好Nginx服务器

## 如果已经配置好服务器

### 修改rtmp.py文件

将localhost改为你的服务器地址，然后将```port```改为你配置的端口

```python
rtmpUrl = "rtmp://localhost:port/videotest/test"
```

### 修改摄像头参数

如果你想要调用自带摄像头，则不用更改。

如果你想要调用其他摄像头，请把

```python
cap = cv.VideoCapture(0)
```

中的0改为1或2

```python
cap = cv.VideoCapture(1)
# or
cap = cv.VideoCapture(2)
```

### 运行

```bash
python rtmp.py
```

然后摄像头的图像便被串流到了服务器上

## 配置服务器

请参见Nginx相关文档
