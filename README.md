# donbosa-bug

#### 파일 복사(일정한 바이트씩 끊어서)

```python
BUF_SIZE = 1024
with open('src.png', 'rb') as sf, open('dst.png', 'wb') as df: # 원본 이미지 파일(src.png을 바이너리 읽기 모드(rb)로 열어서 sf 파일 객체를 생성하고, 대상 이미지 파일(dst.png)을 바이너리 쓰기 모드로 열어서 df 파일 객체를 생성한다.
    while True:
        data = sf.read(BUF_SIZE)
        if not data:
            break
        df.write(data)
```
