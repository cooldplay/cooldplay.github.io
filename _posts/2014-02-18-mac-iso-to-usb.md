---
title: Mac OSX 터미널에서 USB 로 ISO 이미지 굽기
layout: post
---

내가 삽입한 USB 스틱의 볼륨 번호를 확인한다.  ( eg : /dev/disk1 )

```bash
$ diskutil list 
```
이제부터 usb 스틱의 볼륨 번호를 /dev/disk1 이라고 가정한다.


USB 스틱의 마운트를 해제한다. 
```bash
$ diskutil unmountDisk /dev/disk1
```

ISO 이미지를 USB스틱으로 굽는다. ( sudo 권한 필요 )
```
$ sudo dd if=[ISO이미지경로] of=/dev/rdisk1 bs=1m
```
디스크가 구워지는 동안 친절하게도 콘솔에는 아무 정보도 표시되지 않으므로, waiting~

굽기가 완료되면 간단한 결과가 출력된다. 이제 USB 스틱을 Eject 시켜준다.
```
$ diskutil eject /dev/disk1
```

다시 마운트를 시켜보면, 깔~끔하게 구워져 있는 USB스틱의 내용을 확인할 수 있을것이다.