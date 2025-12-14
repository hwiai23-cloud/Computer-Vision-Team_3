## A Geometric Normalization-Based Template Matching Framework for Constellation Recognition

> ComputerVision Team Project team 3

본 프로젝트는 기하학적 정규화(Geometric Normalization) 와 Template Matching 기법을 기반으로,  천체 이미지에서 별자리를 인식하는 컴퓨터 비전 프레임워크를 구현한 팀 프로젝트입니다. 별 간 상대적 기하 구조를 정규화하여 회전·이동·스케일 변화에 강인한 별자리 매칭을 수행하는 것을 목표로 합니다.

### Method Overview

본 프레임워크의 핵심 아이디어는 다음과 같습니다.

- 별자리를 절대 좌표가 아닌 상대적 기하 구조로 표현

- 템플릿 별 좌표를 기준으로 입력 이미지의 별 분포를 정규화

- 정규화된 좌표 공간에서 Template Matching을 수행하여 별자리 식별

이를 통해 조명 변화, 시야 회전, 이미지 스케일 변화에도 비교적 안정적인 인식 성능을 확보하고자 하였습니다.

### Project Structure

```
constellation/
├── demo.ipynb # 전체 파이프라인 실행 데모 노트북
├── test_data/ # 입력 천체 이미지 (테스트용)
├── Templates/ # 별자리 템플릿 데이터
├── Template Coordinates # 템플릿 별 좌표 정보 파일
└── Predicted_images/ # 예측 및 시각화 결과 저장 폴더
```

### Quick Start (프로젝트 실행 방법)

본 프로젝트는 Google Colab 또는 로컬 환경에서 모두 실행할 수 있습니다.

실행 환경에 따라 data_path 설정 방식이 다릅니다.

**Option 1. Google Colab에서 실행하는 경우**

1. 저장소를 Google Drive에 업로드합니다. 

2. `demo.ipynb` 파일을 엽니다.

3. 첫 번째 셀에서 `data_path` 변수에 프로젝트 최상위 폴더(`constellation`)의 경로를 입력합니다.
   
   ```
   data_path = "/content/drive/MyDrive/constellation"
   ```

경로 설정 이후에는 모든 파일이 상대 경로 기반으로 자동 처리됩니다.

**Option 2. Git Clone 후 로컬 환경에서 실행하는 경우**

1. 저장소를 로컬 환경에 clone합니다.

2. `demo.ipynb`를 실행합니다.

3. 로컬에서 실행할 경우, 프로젝트 루트 디렉토리에서 노트북을 실행하면  
   `data_path`를 별도로 설정할 필요가 없습니다.
   
   ```
   data_path = "."
   ```
   
   또는 `data_path`을 위와 같이 두고 실행해도 정상 동작합니다.



### Demo Contents

`demo.ipynb`에서는 다음과 같은 과정을 단계별로 확인할 수 있습니다.

1. 별자리 템플릿 데이터베이스 구성

2. 테스트 천체 이미지 로드 (`test_data`)

3. 별 후보 검출 및 전처리

4. 템플릿 좌표 기반 기하학적 정규화

5. 템플릿 매칭 수행

6. 별자리 인식 결과 시각화 및 저장

## Team Members  (Computer Vision Team 3)

| Name | Student ID | Email                                               |
| ---- | ---------- | --------------------------------------------------- |
| 최다현  | 2277032    | [cdh030303@ewha.ac.kr](mailto:cdh030303@ewha.ac.kr) |
| 김휘서  | 2391010    | [hwiai23@ewha.ac.kr](mailto:hwiai23@ewha.ac.kr)     |
| 차나현  | 2391030    | [cnh0922@ewhain.net](mailto:cnh0922@ewhain.net)     |
| 홍예진  | 2391039    | [2391039@ewhain.net](mailto:2391039@ewhain.net)     |
