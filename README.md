# web-server-app




aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/s0k4s5w7

docker build -t nginx-reverse-proxy .

docker tag nginx-reverse-proxy:latest public.ecr.aws/s0k4s5w7/nginx-reverse-proxy:latest

docker push public.ecr.aws/s0k4s5w7/nginx-reverse-proxy:latest


docker build -t tomcat-web .

docker tag tomcat-web:latest public.ecr.aws/s0k4s5w7/tomcat-web:latest

docker push public.ecr.aws/s0k4s5w7/tomcat-web:latest
