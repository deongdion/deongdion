```py
from datetime import datetime

class Me:
    name: str = "Jeong Jiwon"
    birth: int = 2005
    role: str = "Developer"
    
    @property
    def age(self) -> int:
        return datetime.now().year - self.birth

me = Me()
```
