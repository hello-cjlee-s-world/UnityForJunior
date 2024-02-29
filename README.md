# UnityForJunior

## 초보자를 위한 유니티 입문
#### `병합 전 커밋 내역`
* * *
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
   
3. 병아리 구슬 배치
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
  
* * *
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
* * *
`Stage Run`

1. 에셋 스토어에서 Standard Assets다운
- 존재하지 않음. 어느순간부터 제공하지 않음
- https://github.com/RoadwayVR/UnityStandardAssets 에서 다운받아서 프로젝트 Assets 디렉토리에 붙여넣기해서 임포트 시킴. 해결
- 오브젝트 색이 전부 핑크색으로 나오길래 구글링해보니 해당 오브젝트에 설정된 Material 찾아서 Shader를 standard로 바꿔주라고 함. 해결

2. 바닥 생성
- Standard Assets

3. 캐릭터 생성
- Standard Assets

4. 캐릭터 따라가는 카메라 설정
- 기본 main camera 삭제
- Standard Assets 의 MultipurposeCameraRig 설정.
- 3의 캐릭터 tag에 Player 설정하면 해당 태그의 오브젝트 따라가는 카메라 설정 완료
5. 계단, 길, 집, 결승점 생성

6. 박스 생성

- 박스는 또 1의 링크에서 제공하는 데이터가 없길래 이 책의 저자가 제공하는 프로젝트 소스에서 붙여넣기
7. 계단, 길, 집, 결승점의 텍스쳐 변경
- Asset Store 에서 Yughues Free Architectural Materials(무료) 임포트하여 사용
- 임포트 후 원하는 텍스쳐를 적용할 오브젝트에 어태치 하면 적용 완료

8. 라이트 추가
- 하이어라키 창에서 create -> light 에서 생성 가능
- p287

9. 낙하 판정 영역 생성
- 3D 오브젝트인 cube 생성 후 장판 하단에 영역을 넓게 펼침
- Inspector 창에서 Mesh Renderer를 체크 해제 또는 삭제하면 안보이게 설정 가능
- Inspector의 Box Collider 에서 Is Trigger를 체크하면 기존 충돌 판정이 사라지고 임의의 충돌판정을 script에서 처리 가능

10. 낙하 판정 스크립트 생성
- p304 참고
- 함수에 Collider col 인자 받음 col.gameObject.tag == "Player" 값으로 충돌 감지
- 위의 낙하 영역 오브젝트에 어태치

11. 결승점 생성
- 3D cube 생성 후 Mesh Renderer, Box Collider 설정

12. 골인 스크립트 생성
- p312 참고
- 함수에 Collider col 인자 받음 col.gameObject.tag == "Player" 값으로 충돌 감지
- 위의 결승점 오브젝트에 어태치

13. 타이머 생성
- UI의 Text로 생성

14. 타이머 스크립트 작성
- p320 참고
- 시간 재는 방법 나옴

15. 결과 화면(현재 기록, 최고 기록, 다시하기 버튼) 생성
- 현재,최고 기록 -> UI의 Text로 생성
- 다시하기 버튼 -> UI의 button으로 생성

16. 결과 화면 숨기기
- empty  생성 후 결과 화면 오브젝트들을 자식으로 넣은 후 empty 오브젝트 옆에 체크 해제

18. 결과 화면 처리 스크립트 생성
- p335 참고
- canvas에 스크립트 어태치
