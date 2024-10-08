# Unreal5 Project Template

## 프로젝트 디렉터리 구조

이 프로젝트는 다양한 에셋을 카테고리별로 정리하여 관리하기 위한 템플릿 프로젝트입니다. 각 디렉터리는 특정 기능 또는 시스템에 해당하는 에셋을 포함하며, 하위 디렉터리로 세분화되어 있습니다. 이 README에서는 기본적으로 사용할 **공통 디렉터리 구조**와 **추가 디렉터리 생성 가이드라인**을 제공합니다.

### **기본 디렉터리 구조**

```bash
Content/  
├── Audio/                
│   ├── Ambience/            
│   ├── Music/              
│   └── SFX/           
├── Characters/           
│   ├── Player/           
│   │  ├── Meshes/  
│   │  ├── Animations/  
│   │  ├── Blueprints/  
│   │  ├── Materials/  
│   │  └── Textures/  
│   ├── NPC/              
│   └── Enemies/          
├── Core/                 
│   ├── GameMode/         
│   ├── PlayerController/ 
│   └── SaveGame/         
├── Environments/         
│   ├── Meshes/           
│   ├── Materials/        
│   ├── Textures/         
│   └── Landscapes/       
├── Gameplay/             
│   ├── DataTables/       
│   └── Mechanics/        
├── Maps/                 
├── UI/                   
│   ├── Widgets/          
│   ├── Icons/            
│   └── Fonts/            
├── Utilities/            
└── Weapons/             
    ├── DataTables/       
    └── Mechanics/        
```

## 주요 디렉터리 구조 및 사용 가이드라인

### `Audio/`
- **역할:** 게임 오디오와 관련된 에셋을 관리합니다.
- **설명:** 프로젝트에서 사용하는 모든 음악, 효과음, 음성 파일을 포함합니다.
- **하위 디렉터리:**
  - `Ambience/`: 환경 사운드
  - `Music/`: 배경 음악
  - `SFX/`: 사운드 효과

### **`Characters/`**
- **역할:** 모든 캐릭터 관련 에셋을 관리.
- **설명:** 플레이어 캐릭터, NPC, 적 캐릭터를 구분하여 디렉터리를 생성하고 관리합니다.
- **하위 디렉터리 예시:**
  - `Player/`: 플레이어 캐릭터 관련 에셋 및 블루프린트.
      - **하위 디렉터리:**
    - `Meshes/`: 캐릭터의 3D 모델을 저장
    - `Animations/`: 캐릭터 애니메이션 데이터
    - `Blueprints/`: 캐릭터 관련 블루프린트
    - `Materials/`: 캐릭터에 적용되는 머티리얼
    - `Textures/`: 캐릭터의 텍스처
  - `NPC/`: 일반 NPC 캐릭터 (상인, 대화 NPC 등) 관련 에셋.
  - `Enemies/`: 적 캐릭터 (몬스터, 보스 등) 관련 애니메이션 및 블루프린트.

> **추가 디렉터리:** 특정 상황에 따라 `Allies/`, `Bosses/` 등의 디렉터리를 생성하여 더 세부적으로 관리할 수 있습니다.

### **`Core/`**
- **역할:** 게임의 핵심 시스템과 관련된 블루프린트를 관리합니다.
- **하위 디렉터리:**
  - `GameMode/`: 게임 모드 블루프린트.
  - `PlayerController/`: 플레이어 컨트롤러 관련 블루프린트.
  - `SaveGame/`: 게임 저장 및 불러오기 관련 블루프린트.

### `Environments/`
- **역할:** 게임 환경과 관련된 에셋을 저장하는 디렉터리입니다.
- **하위 폴더:**
  - `Meshes/`: 환경 관련 3D 모델
  - `Materials/`: 환경에 적용되는 머티리얼
  - `Textures/`: 환경 텍스처
  - `Landscapes/`: 지형 관련 에셋

### **`Gameplay/`**
- **역할:** 게임플레이와 관련된 메커니즘 및 시스템 에셋을 관리합니다.
- **하위 디렉터리:**
  - `DataTables/`: 게임에서 사용되는 데이터 테이블을 포함하는 디렉터리입니다.
  - `Mechanics/`: 특정 게임 메커니즘(전투, 탐색, 퀘스트 등) 관련 블루프린트 등을 포함합니다.

> **추가 가이드:** 특정 게임 시스템(예: `Abilities/` 디렉터리) 또는 **각종 아이템(예: `Items/` 디렉터리)**과 같은 디렉터리를 생성하여 추가적인 기능을 확장할 수 있습니다.

### **`Maps/`**
- **역할:** 게임 내 모든 레벨을 포함하는 디렉터리입니다.
- **설명:** 각 레벨에 맞는 맵 블루프린트 및 레벨 파일을 이곳에 저장합니다.

### **`UI/`**
- **역할:** 사용자 인터페이스(UI)와 관련된 에셋을 관리합니다.
- **하위 디렉터리:**
  - `Widgets/`: 위젯 블루프린트.
  - `Icons/`: UI 아이콘.
  - `Fonts/`: UI에서 사용하는 글꼴 파일.

### **`Utilities/`**
- **역할:** 공용으로 사용할 함수 라이브러리, 매크로, 그리고 유틸리티 클래스들을 관리.
- **설명:** 자주 사용되는 **공통 블루프린트 함수**나 **매크로**를 이곳에 정의하여, 다른 시스템에서도 재사용할 수 있도록 합니다.

### **`Weapons/`**
- **역할:** 게임 내 무기 시스템과 관련된 에셋을 관리합니다.
- **설명:** 무기 모델, 애니메이션, VFX, 블루프린트를 포함합니다.
- **하위 디렉터리:**
  - `Meshes/`: 무기 모델 (검, 총, 활 등).
  - `Materials/`: 무기에 적용되는 머티리얼.
  - `Blueprints/`: 무기 로직 블루프린트.
  - `VFX/`: 무기 시각 효과, 충돌 효과.

> **추가 가이드:** 타워 디펜스 게임의 방어 타워와 같은 경우, Towers/라는 별도의 폴더를 생성하여 관리할 수 있습니다.

---

## 추가적인 디렉터리 생성 가이드라인
- 특정 게임의 **독립적인 시스템**이 필요할 경우, 새로운 디렉터리를 생성하여 관리할 수 있습니다. 예를 들어:
  - **AI 시스템**: `Gameplay/AI/` 디렉터리를 생성하여 AI 관련 블루프린트를 관리합니다.
  - **미디어 관리**: `Media/` 미디어 디렉터리를 생성하여 하위 디렉터리로 Audio, Viedo 등을 관리합니다.

## 프로젝트 구조 확장 시 참고 사항
1. **새로운 디렉터리를 생성**할 때는 **디렉터리 목적과 파일 구성을 README에 업데이트**하여, 다른 팀원들이 디렉터리의 용도를 명확하게 이해할 수 있도록 합니다.
2. **디렉터리 구조가 지나치게 깊어지지 않도록 관리**하고, **중복된 파일**이 생기지 않도록 주의하세요.

--- 

위의 구조는 프로젝트의 성격에 따라 언제든지 확장 및 변경할 수 있도록 유연하게 설계되었습니다. 필요에 따라 README에 **특정 기능**에 대한 디렉터리 구조를 명시하고, **팀 내에서 표준화**할 수 있도록 유지보수합니다.