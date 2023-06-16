# IPU 시작하기
본 문서는 IPU를 처음 사용하는 사용자를 위한 가이드 문서입니다. IPU를 사용하기 위한 환경 구성에 대하여 설명드리도록 하겠습니다.

# IPU 사용 현황 확인
IPU 사용을 위해선느 poplar sdk 설치가 필요합니다. poplar sdk는 그래프코어 [다운로드 페이지](https://www.graphcore.ai/downloads)에서 다운 받을 수 있습니다.   
poplar sdk를 다운받으면 IPU도 GPU의 ```nvidia-smi``` 같은 사용 현황을 확인할 수 있는 명령어가 존재합니다.   
```
$ gc-monitor
```
하지만 위 명령어를 실행하였을 때 다음과 같은 결과가 발생합니다.
```
bash: gc-monitor: command not found
```
위 메시지는 poplar sdk를 사용 가능한 상태로 활성화 하지 않았을 때 발생합니다. 설치한 poplar sdk를 사용하기 위해서는 아래와 같은 명령어를 실행해야 합니다.   
poplar sdk version < 2.6
```
$ source [SDK-path]/poplar*/enable.sh
$ source [SDK-path]/popart*/enable.sh
```
poplar sdk version >= 2.6
```
$ source [SDK-path]/poplar*/enable
```


