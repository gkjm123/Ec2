### AWS 의 EC2, S3, Code Deploy 그리고 깃허브의 WorkFlow 를 이용한 자동배포 시스템

1. master 브렌치에 push 또는 merge 시 WorkFlow 에서 감지하여 빌드하고 zip 파일로 만들어 S3 로 전송
2. WorkFlow 가 Code Deploy 에게 배포를 요청
3. Code Deploy 에서 S3 에 올라간 zip 파일을 받아 EC2 로 이동
4. EC2 에서 이미 진행중인 프로세스가 있으면 종료후 새로운 빌드 파일 실행 
