# ReadMe_여왕개미조


+ ### 사용한 파일 경로
> #### 3개년 재무제표, 종목코드 파일을 불러올 때 사용하는 directory_path

```python
from google.colab import drive
import csv

drive.mount('/content/gdrive')
directory_path = '/content/gdrive/My Drive/Colab Notebooks/'
```

> #### 그래프바에 사용된 이미지 파일을 불러올 때 사용하는 코드

```python
img1 = cv2.imread('/content/gdrive/My Drive/Colab Notebooks/bar-' +flag+'.png', cv2.IMREAD_COLOR)
img2 = cv2.imread('/content/gdrive/My Drive/Colab Notebooks/graph_bar.png', cv2.IMREAD_COLOR)
```

따라서 사용하는 데이터 파일

('재무제표_2021.csv', '재무제표_2020.csv', '재무제표_2019.csv', '종목코드.csv', 'graph_bar.png', 'bar-01.png', 'bar-02.png', 'bar-03.png', 'bar-04.png', 'bar-05.png')

모두 구글 드라이브의 Colab Notebooks 폴더에 있어야 한다.  
<br/>
+ ### 프로그램 실행 시 유의사항

#### 1. 프로그램 실행 시간

전문가 투자 의견 메뉴 실행 시, [와이즈리포트](https://comp.wisereport.co.kr/bsfn/company/c1010001.aspx)에서 전문가 투자의견을 받아온다.

이때, 해당 사이트에서 매일 자정 이뤄지는 업데이트로 인해 자정-새벽 2시까지는 사이트에 프로그램 실행에 필요한 수치가 없어 실행 오류가 날 수 있다.

따라서 자정-새벽 2시를 제외한 시간에 프로그램을 실행해야 한다.

#### 2. csv 데이터 파일 확인

프로그램에서 사용한 csv 파일('재무제표_2021.csv', '재무제표_2020.csv', '재무제표_2019.csv', '종목코드.csv')의 경우, 

윈도우 환경에서 연결 프로그램을 엑셀로 설정하고 열었을 때, 한글이 제대로 보이지 않을 수 있다.

그러나 구글 드라이브에 올리고 나서는 읽기 및 수정이 모두 정상적으로 가능하므로,

별도의 연결 프로그램이 없는 윈도우 환경에서는 모든 csv 파일을 구글 드라이브에 올린 후 확인해야한다.
