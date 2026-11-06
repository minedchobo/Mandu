<div align="center">

# 🥟 만두 (Mandu)

**광고 없는 Windows 압축 프로그램**

압축 풀기 · 압축하기 · 자동 풀림 파일 · 손상 ZIP 복구까지

[![다운로드](https://img.shields.io/badge/다운로드-최신_버전-2ea44f?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/minedchobo/Mandu/releases/latest)
![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011%20(x64)-0078D6?style=flat-square&logo=windows&logoColor=white)
![광고 없음](https://img.shields.io/badge/광고-없음-brightgreen?style=flat-square)
![C++](https://img.shields.io/badge/C%2B%2B-CMake-00599C?style=flat-square&logo=cplusplus&logoColor=white)

</div>

---

## 📌 한눈에 보기

만두는 **가볍고 광고가 없는** Windows용 압축 프로그램입니다.

- 탐색기에서 **우클릭 한 번**으로 풀고 묶습니다.
- ZIP, 7Z, RAR, EGG, ALZ 등 **자주 쓰는 형식을 거의 다** 엽니다.
- 설치 없이 **더블클릭만 하면 풀리는 `.exe`** 도 만들 수 있습니다.
- 새 버전이 나오면 **알려 주고 자동으로 업데이트**합니다.

> 이 저장소에는 **설치 파일(Releases)** 이 올라옵니다.
> 소스 코드는 아직 공개하지 않았습니다.

---

## 📥 설치 방법

**필요한 환경** : Windows 10 (1809 이상) 또는 Windows 11, 64비트

1. [**Releases 페이지**](https://github.com/minedchobo/Mandu/releases/latest) 로 갑니다.
2. `Mandu-x.y.z-setup.exe` 를 내려받습니다.
3. 실행해서 설치합니다.

### ⚠️ "Windows의 PC 보호" 창이 뜰 때

설치 파일에 아직 **정식 코드 서명이 없어서** Windows SmartScreen 경고가 뜰 수 있습니다.

1. **추가 정보** 를 누릅니다.
2. **실행** 을 누릅니다.

### 🔒 파일이 진짜인지 확인하기 (선택)

Releases 에 같이 올라오는 `.sha256` 파일의 값과 비교합니다.

```powershell
Get-FileHash .\Mandu-x.y.z-setup.exe -Algorithm SHA256
```

두 값이 같으면 올바른 파일입니다.

---

## ✨ 주요 기능

### 📂 압축 풀기

| 기능 | 설명 |
|---|---|
| 여러 형식 지원 | ZIP · 7Z · RAR · EGG · ALZ · TAR · GZ · BZ2 · XZ 등 |
| 우클릭 풀기 | **여기에 풀기** · **알아서 풀기** · **"폴더 이름"에 풀기** |
| 같은 이름 파일 | 겹치면 덮어쓸지, 이름을 바꿀지 **물어봅니다** |
| 암호 파일 | 암호 관리자가 **저장한 암호를 먼저 시도**합니다 |
| 글자 깨짐 | 파일 이름 **코드페이지**를 직접 고를 수 있습니다 |
| 풀기 알림 | 끝나면 "압축이 풀렸습니다." 알림이 뜨고, 누르면 폴더가 열립니다 |

### 🗜️ 압축하기

| 기능 | 설명 |
|---|---|
| 빠른 압축 | 우클릭 → **이름.zip** / **이름.7z** |
| 멀티 코어 | ZIP 을 여러 코어로 나눠 빠르게 만듭니다 |
| 압축 안 되는 파일 | 이미 압축된 파일은 **자동으로 건너뛰어** 시간을 아낍니다 |
| 분할 압축 | 메일·카페 등 **용량 제한에 맞춘 프리셋** (10MB · 25MB · 50MB …) |
| 압축 후 검사 | 만든 파일을 바로 검사하고, **문제가 없을 때만** 원본을 지웁니다 |
| 암호 걸기 | 암호 ZIP · 암호 7Z |
| 제외 패턴 | 압축에서 뺄 파일을 패턴으로 지정 |

### 📦 자동 풀림 파일 (⭐ 대표 기능)

받는 사람이 **만두가 없어도** 됩니다.

1. 우클릭 → **이름.exe 자동 풀림으로 압축하기**
2. 받는 사람이 `.exe` 를 **더블클릭**
3. 같은 폴더에 내용물이 바로 풀립니다.

> 인터넷에서 받은 자동 풀림 파일은 서명이 없어서 SmartScreen 경고가 뜰 수 있습니다.

### 🛠️ 도구

- **🩹 손상 ZIP 복구** : 목록(중앙 디렉터리)이 망가진 ZIP 도 남은 내용을 최대한 살려서 엽니다.
- **🔑 암호 관리자** : 암호를 PC 에 **암호화해서** 저장합니다 (Windows DPAPI).
- **🔓 비밀번호 찾기** : **내가 잊어버린** 옛 방식(ZipCrypto) ZIP 암호를 찾아 줍니다. AES 암호 ZIP 은 지원하지 않습니다.
- **✅ 압축 파일 테스트** : 결과를 표로 보여 줍니다 (예상 CRC / 실제 CRC).
- **🛡️ 바이러스 검사** : Windows 에 등록된 백신(AMSI)으로 압축 파일 안을 검사합니다.
- **#️⃣ 파일 해시 확인** : CRC32 · MD5 · SHA-1 · SHA-256 을 계산하고 비교합니다.
- **⏱️ 압축 속도 측정** : 내 PC 에서 압축과 풀기가 얼마나 빠른지 재 봅니다.

### 🖥️ 화면

- 폴더 **트리 + 목록** 보기, 칼럼 선택
- **자세히 / 큰 아이콘 / 썸네일** 보기 방식
- 그림 파일 **미리 보기**
- **다크 테마** 지원 (설정에서 밝게 · 어둡게 · Windows 따름)
- 압축 파일 위로 파일을 **끌어다 놓기**
- Windows 11 **첫 번째 우클릭 메뉴**에도 표시

---

## ⌨️ 명령줄 도구 `mdu`

설치하면 `mdu.exe` 도 같이 설치됩니다.

```text
mdu l <압축 파일>                         내용 목록
mdu t <압축 파일> [-p 암호]                무결성 테스트
mdu x <압축 파일> [-o 폴더] [-p 암호] [-y]  풀기
mdu a <압축 파일> <파일...> [-l 0-9] [-p 암호] [-v 크기] [-t]   압축
mdu crack <ZIP> [-c dlus] [-min N] [-max N]  잊은 ZipCrypto 암호 찾기
```

| 옵션 | 뜻 |
|---|---|
| `-o` | 풀 폴더 |
| `-p` | 암호 |
| `-y` | 묻지 않고 덮어쓰기 |
| `-l` | 압축 수준 (0~9) |
| `-v` | 분할 크기 |
| `-t` | 압축 후 오류 검사 |

---

## 🔄 자동 업데이트

- 프로그램을 쓰면 **하루에 한 번** 새 버전이 있는지 확인합니다.
- 새 버전이 있으면 알림이 뜹니다. 누르면 **바뀐 점**을 보고 업데이트할 수 있습니다.
- 내려받은 설치 파일은 **해시를 검증**한 뒤에 실행합니다.

---

## 🧱 만든 방법

- **언어** : C++ (Win32)
- **빌드** : CMake · Visual Studio · x64
- **설치 파일** : Inno Setup 6
- **압축 엔진**
  - ZIP : 직접 구현한 병렬 엔진 (zlib-ng · libdeflate)
  - 7Z · RAR 등 : 7-Zip 엔진
  - EGG · ALZ 등 : 직접 구현
- **탐색기 우클릭 메뉴** : 셸 확장 DLL + Windows 11 용 패키지

---

## 🙏 오픈소스와 라이선스

만두는 아래 소프트웨어를 사용합니다. 자세한 고지문은 설치 폴더의 `THIRD_PARTY_NOTICES.txt` 에 있습니다.

| 이름 | 쓰는 곳 | 라이선스 |
|---|---|---|
| [7-Zip](https://www.7-zip.org/) | 7Z · RAR 등 처리 | GNU LGPL (+ unRAR 제한) |
| [zlib-ng](https://github.com/zlib-ng/zlib-ng) | ZIP 압축 · 해제 · CRC | zlib License |
| [libdeflate](https://github.com/ebiggers/libdeflate) | 작은 파일 ZIP 압축 | MIT |
| bzip2 | BZip2 · ALZ | BSD 계열 |
| LZMA SDK | LZMA | 공개 도메인 |

> **EGG 형식 해제**는 ESTsoft 의 라이선스 조건에 따라 **비상업적 용도**로만 사용할 수 있습니다.

> 만두는 다른 압축 프로그램과 **관련이 없는 독립 프로그램**입니다.
> 다른 프로그램의 동작과 화면 배치를 참고했을 뿐, **그 프로그램의 코드를 가져오지 않고 새로 만들었습니다.**

---

## 💬 문의와 제안

버그나 바라는 점은 [**Issues**](https://github.com/minedchobo/Mandu/issues) 에 남겨 주세요.

<div align="center">

🥟 **만두와 함께 가볍게 압축하세요**

</div>
