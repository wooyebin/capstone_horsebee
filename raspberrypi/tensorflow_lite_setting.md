## Tensorflow Lite runtime install
+ 환경
  + raspberrypi 3B
  + ubuntu desktop 22.04
* * *
### 파이썬 버전 확인   
```python3 -V```   
> + 3.5 ~ 3.8 가능   
> + 만약 3.5 ~ 3.8 아니면 3.7을 설치해보도록 하자   
> + https://codechacha.com/ko/ubuntu-install-python39/ 참고   
>>  ```sudo apt install software-properties-common```   
  ```sudo add-apt-repository ppa:deadsnakes/ppa```   
  ```sudo apt install python3.7```   
  ```sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 3```   
  ```sudo update-alternatives --config python3```   
  ```python3 -V```   
   
* * *
### 아키텍처 확인  
```uname -m```   
   
* * *
### tensorflow lite runtime 설치   
파이썬 버전과 아키텍처 정보 가지고 아래 링크 알맞는 URL 찾아야함   
ex) 위의 방법을 따랐다면 Linux(ARM 64) Python3.7임   
https://www.tensorflow.org/lite/guide/python?hl=ko 참고   
```pip3 install 	https://dl.google.com/coral/python/tflite_runtime-2.1.0.post1-cp37-cp37m-linux_aarch64.whl```   
> + 만약 안되면 pc에서 파일 다운 받아서 rasp으로 옮긴 후   
>> ```pip3 install <경로 ex) /home/horsebee/Downloads/tflite_runtime-2.1.0.post1-cp37-cp37m-linux_aarch64.whl>```   

```python3```   
```>>> from tflite_runtime.interpreter import Interpreter```   
