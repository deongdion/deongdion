```py
from datetime import datetime
from dataclasses import dataclass
from typing import List

@dataclass
class Vulnerability:
    company: str
    severity: str
    description: str

class Me:
    name: str = "정지원"
    birth: int = 2005
    role: str = "Developer" # 객체 지향 프로그래머 !
    skills: List[str] = ["Python", "C#", "WPF", "MongoDB"]
    
    vulnerabilities: List[Vulnerability] = [
        Vulnerability(
            company="이스트소프트 (ESTsoft)",
            severity="Critical",
            description="에이쁠포인트 앱 포인트 환전 로직에서 음수 입력 및 integer overflow를 이용해 포인트 무한 생성이 가능하며, 서버 측 입력값 검증 부재로 외부 결제 수단(네이버 페이)으로의 전환까지 가능한 무결성 훼손 취약점 제보 및 솔루션 제공"
        ),
        Vulnerability(
            company="넥슨 (NEXON)", 
            severity="Medium",
            description="서든어택 알려듀오 웹 게시판에 position:fixed div 삽입으로 전체 화면을 투명하게 덮어 사용자 클릭을 가로채는 clickjacking 취약점을 통해 계정 정보 변경 및 결제 등 민감 기능 강제 실행 가능성 제보"
        ),
        Vulnerability(
            company="대체불가능회사",
            severity="Critical", 
            description="코퀴즈 (Coquiz) 앱 아이템 거래 로직 내 signed/unsigned 변환 처리 미흡을 이용해 음수 입력 시 최대값으로 캐스팅되는 취약점을 통해 약 1,000만 Conut 코인(2026.03.10 기준 약 2.6억 원) 규모의 잔액 증폭 및 전체 자산 탈취를 재현하였으며, 검증 부재로 무제한 재화 생성이 가능한 경제 시스템 붕괴 수준의 취약점 제보 및 타입 캐스팅 검증 로직 제안"
        ),
        Vulnerability(
            company="파이널나인",
            severity="Critical",
            description="(구)파이널나인 앱 시드머니 거래 시 음수 값 검증 부재로 무제한 포인트 획득 가능 및 (신)파이널나인-F9 앱 클라이언트 측 Firebase 직접 호출로 인한 전체 이용자 개인정보 노출 취약점을 사전 분석 단계에서 발견하여 제보"
        ),
        Vulnerability(
            company="헤즈업",
            severity="High",
            description="헤즈업 홀덤 앱 비밀번호 변경 프로세스에서 본인 확인 절차 부재로 타인의 계정 비밀번호를 임의로 변경 가능한 계정 탈취 취약점을 사전 분석 단계에서 발견하여 제보"
        )
    ]
    
    @property
    def age(self) -> int:
        return datetime.now().year - self.birth
```
