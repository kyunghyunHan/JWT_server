
- go get github.com/gin-gonic
# JWT_server
- 사용자가 id와 password를 입력하여 로그인을 시도
- 서버는 요청을 확인하고 secret key를 통해 Access token을 발급
- JWT 토큰을 클라이언트에 전달
- 클라이언트에서 API 을 요청할때  클라이언트가 Authorization header에 Access token을 담아서 전달
- 서버는 JWT Signature를 체크하고 Payload로부터 사용자 정보를 확인해 데이터를 반환
- 클라이언트의 로그인 정보를 서버 메모리에 저장하지 않기 때문에 토큰기반 인증 메커니즘을 제공
- 인증이 필요한 경로에 접근할 때 서버 측은 Authorization 헤더에 유효한 JWT 또는 존재하는지 확인
- JWT에는 필요한 모든 정보를 토큰에 포함하기 때문에 데이터베이스과 같은 서버와의 커뮤니케이션 오버 헤드를 최소화 
- Cross-Origin Resource Sharing (CORS)는 쿠키를 사용하지 않기 때문에 JWT를 채용 한 인증 메커니즘은 두 도메인에서 API를 제공하더라도 문제가 미발생
- 일반적으로 JWT 토큰 기반의 인증 시스템은 위와 같은 프로세스로 기반
- 처음 사용자를 등록할 때 Access token과 Refresh token이 모두 발급되어야함
