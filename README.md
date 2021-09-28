# 세부적 버전 관리 (Detailed Version Management 2.0.0)

0. 구조  
 1). Major.Minor.Patch_Identifier.Metadata.Build    
 2). Major, Minor, Patch는 MainPart로 묶는다.  
 3). Identifiter, Metadata, Build는 SubPart로 묶는다.  
  
1. Major에는 숫자를 붙이며 앞에 0을 쓰지 않는다.  
 1). Major 버전은 이전까지의 버전과 호환이 되지 않을 때, 혹은 큰 변경점이 생겼을 때에 상승한다.  
 2). Major가 0일 때에는 개발용으로 쓰며, Identifier을 Personal로 유지한다.  
 3). Major 버전이 상승하면 Minor, Patch의 숫자를 0으로 만든다.  
 4). 버전이 9를 넘었을 경우에는 10, 11...을 쓰며 이전 버전에서는 자릿수를 맞출 필요가 없다.  
  
2. Minor에는 숫자를 붙이며 앞에 0을 쓰지 않는다.  
 1). Minor 버전은 기능의 추가, 삭제 및 수정이 발생했을 때에 상승한다.  
 2). Major가 같은 버전끼리는 호환이 되어야 한다.  
 3). 초기 버전은 0.1.0이므로 Minor 버전은 1로 해야한다.  
 4). Minor 버전이 상승하면 Patch의 숫자를 0으로 만든다.  
 5). 버전이 9를 넘었을 경우에는 10, 11...을 쓰며 이전 버전에서는 자릿수를 맞출 필요가 없다.  
  
3. Patch에는 숫자를 붙이며 앞에 0을 쓰지 않는다.  
 1). Patch 버전은 버그 수정 및 개선을 할 때에 상승한다.  
 2). Minor가 같은 버전끼리는 기능이 같거나 비슷해야한다.  
 3). Patch 버전이 상승하면 SubPart의 내용을 초기화한다. [Minor와 Major도 마찬가지이다.]  
 4). 버전이 9를 넘었을 경우에는 10, 11...을 쓰며 이전 버전에서는 자릿수를 맞출 필요가 없다.  
  
2. Identifier는 두 가지 방식 중 한 가지를 선택하는 것으로 한다.  
 1). Personal, Private, Protected, Public, Release을 붙인다.  
  (1). Personal : Metadata를 붙힐 수 없으며, 개인용으로 쓴다.  
  (2). Private : MetaData를 붙힐 수 있으며, 내부 실험용으로 쓴다.  
  (3). Protected : MetaData를 붙힐 수 있으며, 프로그램 안정화용으로 쓴다.  
  (4). Public : MetaData를 붙힐 수 있으며, 외부 실험용으로 쓴다.  
  (5). Release : MetaData를 붙힐 수 없으며, 공개용으로 쓴다. 또한, Release 버전일 때에는 SubPart의 내용을 생략한다.  
  (6). Identifier 버전이 다음 버전으로 넘어간다면 Metadata의 숫자를 A0으로 만든다.  
 2). Dev, Daily, Nightly, Alpha ~ Omega, Release를 붙힌다.  
  (1). Dev : Metadata를 붙힐 수 없으며, 배포를 하지 않는 용도다.  
  (2). Daily, Nightly : Metadata를 붙힐 수 있으며, Build는 2) 규칙을 따라야한다.  
  (3). Alpha ~ Omega : 각 팀 혹은 개인의 원칙에 따라 분류한다.
  (4). Release : 이때에는 Identifier이 생략되며 공개용일 때에 사용한다.
  
3. Metadata는 Identifier가 Private, Protected, Public일 때에 붙으며 한 자리 알파벳과 한 자리 숫자로 표현한다.  
 1). 버전이 Release되기 전에 내용의 변화가 일어났을 때에만 상승한다.  
 2). 숫자가 9일 경우에는 알파벳을 상승시키고 숫자를 0으로 변경한다.  
 3). 버전이 Z9를 넘었을 경우에는 알파벳을 제외하고 10, 11...을 쓰며 이전 버전에서는 자릿수를 맞출 필요가 없다.  
  
4. Build는 두 가지 방식 중 한 가지를 선택하는 것으로 한다. 
 1). 버전이 바뀔 때마다 숫자를 하나씩 높인다.  
 2). 연도와 월일을 사용한 8자리 숫자를 이용한다.  

5. 주요 규칙  
 1). 버전을 빌드하여 배포하는 순간 해당 버전은 수정되어서는 안된다.  
 2). 상단의 버전 표기 규칙을 실수로 어기게 될 경우, 배포한 버전은 놔둔다. 그리고 해당 사항에 맞는 버전을 올려 재배포한다.  
 3). Major가 0일 때에는 개발자가 원할 때에 버전을 변경할 수 있으나 가급적이면 규칙은 지키는 것을 원칙으로 한다.  
 4). Build 버전은 차용하지 않아도 되며 해당 버전은 생략 혹은 방치해도 무관하나 이때에는 해당 버전을 공개해서는 안된다. [사용자가 봤을 때에는 업데이트가 안 됐다고 생각할 수 있기 때문이다.]  
 5). 버전을 관리하는 도중 이전 버전에 문제가 생기면서 해당 버전을 임의적으로 수정한 경우에도 버전은 반드시 변경해야만 한다.  
 6). 해당 문서는 유의적 버전 관리 2.0을 세부화시킨 문서이며 사용하고자 하는 사용자만 참고하여 사용하면 된다.  
 7). 해당 문서는 폴더 정렬 규칙에 의거하여 작성되었다.  
  
이 문서는 개인 저장용으로 사용되고 있습니다.  
마음에 드신다면 사용하시되 해당 문서의 내용을 참조했다는 것을 명시해주시면 감사하겠습니다.  
또한, 이 문서는 '유의적 버전 2.0' 문서에서 감명받아서 만들었음을 알립니다.  
  
P.S. 사실 이 버전 관리법을 node.js package에서 사용하면 거기서는 '유의적 버전 2.0'만 허용하기 때문에 먹히지 않는다...  
