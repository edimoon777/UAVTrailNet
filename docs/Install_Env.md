
# 기본적인 프로그램 환경
## 크롬 설치
구글 크롬 브라우저를 설치합니다.
```
   wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb   
   sudo dpkg -i google-chrome-stable_current_amd64.deb
```

## git 설치
오픈 소스와의 연동 및 업데이트를 위해 필수적으로 필요합니다.    
```
sudo apt-get install git
```
## PyCharm 설치
아래 명령어를 이용해 설치합니다.   
```
sudo snap install pycharm-community --classic
```   
Pycharm 실행 명령어는 다음과 같습니다.
```
pycharm-community
```   


## Virtual Environment 설치
pip 및 Virtualenv 설치
```
sudo apt-get install python-pip python-dev python-virtualenv
sudo apt-get install python3-pip python3-dev python-virtualenv
```

가상환경(virtual environment) 생성 (루트 디렉토리 에서 실행하기)
여기서 'ENVNAME' 부분은 원하는 환경이름을 적어준다.   
```
virtualenv ENVNAME --python=python3.5
```

가상환경은 필요에 따라 활성화/비활성화를 할 수 있습니다.   
가상환경 활성화 방법   
```
source ENVNAME/bin/activate
```
가상환경 비활성화 방법
```
deactivate
```
   
# GPU를 이용한 딥러닝 환경
## 그래픽 드라이브 설치
   

## CUDA 설치   

CUDA 9.0을 다운로드해 설치합니다.  [[Download CUDA 9.0 Ubuntu 16.04]](
https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=deblocal)

설치파일의 형식에 따라 설치 방법이 다르다. 다음 명령을 참고하여 설치한다.     
설치방법1. run파일   
```
sudo sh cuda_9.0.176_384.81_linux.run
```

설치방법2. deb파일 
```
sudo dpkg -i cuda-repo-ubuntu1604-9-0-local_9.0.176-1_amd64.deb
sudo apt-key add /var/cuda-repo-9-0-local/7fa2af80.pub
sudo apt-get update
sudo apt-get install cuda
```

설치 여부 확인방법은 아래와 같이 버전이 표시되면 정상적으로 설치된 것입니다.   
`nvcc --version`
>nvcc: NVIDIA (R) Cuda compiler driver   
>Copyright (c) 2005-2015 NVIDIA Corporation   
>Built on Tue_Aug_11_14:27:32_CDT_2015   
>Cuda compilation tools, release 7.5, V7.5.17   

## CUDNN 설치
CuDNN 설치 버전 확인 방법입니다. 
```
cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2 --
```
> #define CUDNN_MAJOR 7   
> #define CUDNN_MINOR 1   
> #define CUDNN_PATCHLEVEL 3   
> --   
> #define CUDNN_VERSION    (CUDNN_MAJOR * 1000 + CUDNN_MINOR * 100 + CUDNN_PATCHLEVEL)   
>      
> #include "driver_types.h"   



# 
