## 배포 링크
https://solar-connect-1.netlify.app/

## 프로젝트 소개
원티드 프리온보딩 프론트엔드 코스에서 **정렬, 날짜 기능**을 구현한 과제입니다.<br />
과제는 페어프로그래밍으로 진행됐습니다.
정렬의 경우 초기에는 간단한 작업이므로 빠르게 구현할 수 있는 버블 정렬 알고리즘을 사용했으나 회의를 통해 다음과 같은 이유로 병합 정렬(merge sort)로 변경했습니다.
- 병합 정렬의 시간 복잡도는 O(nlog₂n)으로 기본 정렬 알고리즘에 비해 성능이 좋은 편에 속합니다. 
- 또한 이는 어떠한 경우에도 동일하게 적용됩니다. (안정적)

## 기능
1.타이머
  - 재사용성을 위해 컴포넌트 분리
  - 날짜 데이터를 영어로 표기하기 위해 DateTimeFormat을 활용
  
2.정렬
- 허용되지 않는 문자는 자동 제거되도록 구현 (허용: 숫자와 comma(,))
- ' , '를 기준으로 입력값 구분
- 초기 버전에서는 문자열을 숫자로 변경하기 위해 parseInt를 사용했으나 이 경우 문자와 숫자가 동일한 인덱스에 사용될 때 예외처리를 하지 않는 버그가 발생 
- 이 문제를 해결하고자 Number로 변경
- 공백을 0으로 인식하는 버그 replace 메소드 사용해 모든 공백을 한칸으로 변경, 조건문을 통해 한칸 공백은 리턴하지 않도록 하는 방식으로 해결
- 입력값이 잘못된 형식일 경우 예외처리(문자와 숫자가 한꺼번에 입력된 경우와 공백 인식 대응/유효성 검사를 사용할 경우에는 입력값 길이에 대한 제한이 걸려 사용성에 제한이 있다고 판단해 함수로 해결했습니다, 단 소수점&마이너스와 같은 기호는 사용 가능)
- setTimeOut을 통해 출력 시간 제어
- 출력 대기시 버튼 비활성화

## 설치 및 실행
`npm install -> npm start` 


## Contributors
| Contributors| Task                               |
| ----------- | ---------------------------------- |
| 이주영      | 정렬 기능, 한글, 영문 Date 보여주기 |
| 황윤성      | 정렬 기능, 한글, 영문 Date 보여주기 |

## 참고 사이트
https://im-developer.tistory.com/134
