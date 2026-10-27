# Statue of Liberty — Pop-out 3D Illusion

스마트폰 모양의 **가상 프레임** 위에 자유의 여신상 3D 모델이 솟아오르는 착시 체험입니다.

## 파일 구조

```text
statue-liberty-popout-3d/
├── index.html
├── README.md
└── statue_of_liberty_1.glb   ← 사용자가 업로드할 실제 모델
```

## 설치

1. GitHub 저장소 `ilmac-knu/statue-liberty-popout-3d`에 `index.html`, `README.md`를 업로드합니다.
2. 기존 자유의 여신상 모델을 `statue_of_liberty_1.glb`라는 **정확한 이름**으로 저장소 최상위에 업로드합니다.
3. Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save.
4. 배포 후 `https://ilmac-knu.github.io/statue-liberty-popout-3d/`에 접속합니다.

## 조작

- 드래그/한 손가락: 여신상 회전
- 마우스 휠/두 손가락: 확대·축소
- 버튼: 위치 초기화, 회전, 확대, 축소, 프레임 숨김

## 구현 방식과 한계

Three.js로 가상 스마트폰, 받침대, GLB를 동일한 3D 공간에 배치하고 원근감과 그림자로 입체 착시를 만듭니다. 일반 화면의 물리적 경계 밖으로 영상이 실제 출력되지는 않습니다.

GLB를 불러오지 못하면 **임시 자유의 여신상 모형**이 표시됩니다. 정확한 파일명과 경로를 확인하세요. 인터넷 연결이 있어야 Three.js CDN을 불러올 수 있습니다.

이 버전은 테두리 걸침형 첫 시제품입니다. 실제 사진과 같은 고품질 연출을 위해서는 모델 방향·스케일, 화면 배경, 가림 관계를 추가 조정할 수 있습니다.
