# Build
mvn clean package && docker build -t com.airhacks/pirates .

# RUN

docker rm -f pirates || true && docker run -d -p 8080:8080 -p 4848:4848 --name pirates com.airhacks/pirates 