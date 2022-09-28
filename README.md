# nestjs-solutions


### 1.
#### Error Message
QueryFailedError: could not create unique index 

#### Cuase
unique index가 없었는데 업그레이드 과정에서 indexing할 때 중복된 값이 있는 경우


### 2.
#### Problem
NestJs에서 Unit Test할 때 의존성 관련 에러 발생

#### Cause
When running tests the test code won't be able to locate the correct service(s) at run-time. It needs fully relative paths without an absolute 'src/' at the beginning.

If VSCode autocompletes your imports as src/xyz/abc/service.ts instead of ../xyz/abc/service.ts.

#### Solution
import할 때 src를 지우고 상대경로로 변경
