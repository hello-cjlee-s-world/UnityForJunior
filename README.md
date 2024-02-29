# UnityForJunior

## 초보자를 위한 유니티 입문
#### `병합 전 커밋 내역
`ChickAttack`
중간 커밋
1. 프로젝트 만들기.
2. 외부 이미지 불러와 스프라이트 나누기
3. 배경 배치
- 레이어(Order in Layer로 레이어 순서 정하기)
4. 바닥 배치
- 바닥에 충돌 판정 설정(Add Component로 Physics 2D->Box Collider 2D 설정)
5. 자동차 배치
6. 포탑 배치
- 자동차와 포탑을 부모 자식 설정(드래그 앤 드랍)
- 포탑에 충돌 판정 설정(Add Component로 Physics 2D -> Polygon Collider 2D 설정 -> 이미지 모양대로 충돌 판정 잡힘)
7. 카메라 비율 설정
8. 자동차 이동 스크립트 작성 -> 140p 참고
9. 오브젝트에 스크립트 적용
10. 포탄 배치
- 중력이 작용하도록 (Add Component로 Physics 2D -> Rigidbody 2D 설정)
- 원 형태의 충돌 판정 설정(Add Component로 Physics 2D -> Circle Collider 2D 설정)
- 프리펩으로 만들기(assets창에 드래그앤 드랍)
11. 포탄 발사, 사라짐 스크립트 작성 155p, 162p 참조

완성 커밋
1. 경사면 배치
2. 병아리 구슬 배치
- RIgidbody 2D(중력) 추가, Circle Collider 2D(충돌 판정) 추가
- 프리펩 생성
3. 병아리 생성 스크립트 작성
- 병아리 프리펩 넣어줄 GameObject 변수 작성
- InvokeRepeating(함수명, 초기 시작 시간, 실행 주기) 함수로 병아리 구슬 반복 실행
- Instantiate 함수로 반복해서 병아리 구슬 만들 함수 작성
4. 하이어라키에 스크립트 설정할 오브젝트 생성
- 스크립트 오브젝트에 설정
5. 병아리 구슬 마찰, 반발 설정
- Assets 에서 Physics Material 2D 생성, 병아리 프리펩(ChickBallPrefab)에 어태치
- 포탄 발사, 사라짐 스크립트(DestoryObj) 병아리 프리펩에 설정 후 시간 변경 --> 프리펩에 설정 후 시간 변경해도 기존 DestoryObj에는 영향 주지 않음

`ChickUI`
ChickAttack UI 완성
p186 ~ p242
1. 프로젝트 export/import 실습
2. 새로운 신 생성
- 신(Scene)들은 파일로 저장되며 하이어라키에 개별적으로 뜨지 않고 Assets에 뜬다.
3. 타이틀 이미지 배치
- UI -> Image 생성
- Image 오브젝트 인스펙터에 타이틀 이미지 드래그 앤 드롭
- Anchor 상단 중앙 고정
4. 시작 버튼 배치
- 버튼 색, 마우스 올렸을때 바뀌는 색 등 실습
- Anchor 상단 중앙 고정
5. 배경 색 변경
- UI -> Panel 으로 배경 생성
- 하이어라키 상단으로 옮겨 화면상 제일 뒤에 위치하도록 조정
6. 게임 시작 스크립트 생성
- using Unityegine.SceneManagement 라이브러리 임포트해줘야함
- SceneManager.LoadScene("신 이름") 으로 신 변경
7. 버튼에 스크립트 적용
- 버튼 오브젝트에 스크립트 어태치하여 적용하기
- button 컴포넌트의 On Click() 에서 버튼 이름 찾아서 고르고 함수 설정
8. Build setting 변경
- 기존 SampleScene 제거 후 변경할 신들 드래그앤 드랍 후 창 닫기
- 위에서부터 순서대로 신이 이동하므로 순서 맞춰주기