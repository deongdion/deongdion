# 소개

```py
from datetime import datetime

class Me:
    name: str = "정지원"
    birth: int = 2005
    role: str = "개발자"
    
    @property
    def age(self) -> int:
        return datetime.now().year - self.birth

me = Me()
```

### 보안 취약점 제보

**이스트소프트 (ESTsoft)**  
> 포인트 환전 로직에서 음수 입력 및 integer overflow를 이용해 포인트 무한 생성이 가능하며, 서버 측 입력값 검증 부재로 외부 결제 수단(네이버 페이)으로의 전환까지 가능한 무결성 훼손 취약점 제보 및 솔루션 제공

**NEXON - 서든어택 알려듀오 페이지**  
> 게시판에 position:fixed div 삽입으로 전체 화면을 투명하게 덮어 사용자 클릭을 가로채는 clickjacking 취약점을 통해 계정 정보 변경 및 결제 등 민감 기능 강제 실행 가능성 제보

**코퀴즈 (Coquiz)**  
> 아이템 거래 로직 내 signed/unsigned 변환 처리 미흡을 이용해 음수 입력 시 최대값으로 캐스팅되는 취약점을 통해 약 1,000만 코인(약 2.6억 원) 규모의 잔액 증폭 및 전체 자산 탈취를 재현하였으며, 검증 부재로 무제한 재화 생성이 가능한 경제 시스템 붕괴 수준의 취약점 제보 및 타입 캐스팅 검증 로직 제안
