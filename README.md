# Multi-Q-table-Q-learning-Algorithm
* data/factory_order_test.csv : test 데이터
* data/factory_order_train.csv : train 데이터
* data/obstacles.csv : 장애물 위치 좌표
* result_gif : MQQ 결과물 디렉토리
* Multi_Q-table_Q-learning-Algorithm : MQQ 알고리즘의 실행 노트북 파일



# MQQ 아이디어
MQQ는 Q-learning으로 기업 과제를 해결하기 위한 창작의 고뇌를 줄기던 중 번뜩 떠오른 아이디어입니다.   

아이디어는 현재 위치에서 아이템 위치까지 exploration을 하고,   
수렴에 도착했을 때 exploit을 하는 과정을 item 개수만큼 반복하면 해결할 수 있다고 생각했습니다.   

멘토링 과정에 이 아이디어를 말씀드리자 비슷한 논문인 MQQ를 주셨습니다. 🙇‍♂️ ~~(사람 생각하는건 다 비슷하구나...)~~   
참고할 논문이 있어서, 시도한 다른 방법론들보다 비교적 더 원활하게 MQQ를 개발했습니다.

![image](https://user-images.githubusercontent.com/44988108/172668794-c398c569-276a-4fb4-9807-1672f4000fed.png)

![image](https://user-images.githubusercontent.com/44988108/172668794-c398c569-276a-4fb4-9807-1672f4000fed.png)

## Q-table 시각화
![image](https://user-images.githubusercontent.com/41228208/172742632-046ad4db-a614-4b24-9987-ae786e4a37d0.png)

MQQ를 구현하면서 Q-learning을 통한 Q-table이 제대로 보여지는지 확인하기 위해 Q-table을 시각화하여 결과를 확인했습니다.   
Q-table 시각화 영역을 보시면 시작 위치인 'S'부터 'A'까지 갈 수 있는 경로를 표현해주고 있습니다.

## [A,B,F,G,H,I,K] EPI_270 결과 gif  
![00270_MQQ_test_AVG_final_](https://user-images.githubusercontent.com/96896665/172498019-5bb1395c-f8a7-4ee4-ad86-484a6769e593.gif)
>        테스트 결과 :  전체 EPI 1225개 평균 스텝 수 : 44.30342577487765

## MQQ, PQ 장단점
![image](https://user-images.githubusercontent.com/44988108/172670671-17cf4667-544a-4067-adc8-e63c1c57dd45.png)

MQQ는 exploit과 exploration을 반복한다는 특징을 갖고 있기 때문에 train이 필요 없고, test만 돌려도 결과가 나옵니다!   
하지만 이러한 특징 때문에 PQ에 비해 상대적으로 시간이 더 소요된다는 특징을 갖고 있습니다.


<!-- ## MQQ 아이디어 도식화
![image](https://user-images.githubusercontent.com/96896665/172497638-9d744efb-cb8d-4411-8e08-d0270effd53d.png)
 -->
## MQQ 알고리즘 플로우차트
![image](https://user-images.githubusercontent.com/96896665/172497430-34378603-bc0b-4d27-9241-9ea80e31e074.png)
![image](https://user-images.githubusercontent.com/96896665/172497497-582f1554-83d9-477c-b75c-ee6eac2d26dd.png)




# Reference
* https://www.semanticscholar.org/paper/Multi-Q-Table-Q-Learning-Kantasewi-Marukatat/b6eb908216575a29b1df54c32d0e60bb1a3aac8f
