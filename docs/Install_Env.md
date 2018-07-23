
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

   
# GPU를 이용한 딥러닝 환경
## 그래픽 드라이브 설치
   

## CUDA 설치   

CUDA 9.0을 다운로드해 설치합니다.  [[Download CUDA 9.0 Ubuntu 16.04]](
https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=deblocal)

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
