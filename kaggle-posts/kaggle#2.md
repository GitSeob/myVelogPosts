진행하기 앞서 **Tensorflow**을 사용하기 위해 터미널에서 다음의 명령어를 통해 학습 환경을 다운로드하였습니다.

```
# Requires the latest pip
pip install --upgrade pip

# Current stable release for CPU and GPU
pip install tensorflow

# Or try the preview build (unstable)
pip install tf-nightly
```

> 음 ... 클러스터의 wifi를 이용하니 굉장히 오래걸렸다. 한 25분 정도?

```
docker pull tensorflow/tensorflow:latest-py3  # Download latest stable image
docker run -it -p 8888:8888 tensorflow/tensorflow:latest-py3-jupyter  # Start Jupyter server
 ```
 
 명령어를 실행하고 터미널 창에 뜨는 해시된 토큰을 통해 password를 입력하고 할당된 `localhost:할당포트`로 접속하면 다음과 같이 페이지가 로드된다.
 
![](https://images.velog.io/images/anjoy/post/07c46688-c2ab-4d3b-bd62-e0fd73aebea7/image.png)

본격적으로 타이타닉 데이터를 분석해보기 전에 기초가 많이 부족한 상태이기 때문에 다른 문서를 참고하여 공부를 해보려하였습니다.

캐글의 Competition 중 **2019 1st ML month with KaKR**에서 `Hotness` 기준으로 가장 상단에 노출되는 [2019 ML month 대구 튜토리얼을 위한 커널](https://www.kaggle.com/daehungwak/guide-kor-dg)의 Notebook을 참고하여 학습을 진행해보았습니다.


#### 사용되는 Python Module
+ **mayplotlib, seaborn, plotly** : 시각화 도구
+ **pandas, numpy** : 데이터 분석 도구
+ **skelarn, keras** : 모델 개발 도구

> # docker를 통해 tensorflow image로 작업을하다가 따로 백업을 하기 전 실수로 Shutdown이 되어서 학습 중 작성한 코드와 notebook Markdown text가 모두 증발해버렸다...
