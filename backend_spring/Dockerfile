# Sử dụng JDK 21 làm base image
FROM eclipse-temurin:21-jdk

# Cài đặt Maven
RUN apt-get update && apt-get install -y maven

# Đặt thư mục làm việc trong container
WORKDIR /app

# Sao chép mã nguồn vào container từ thư mục backend_spring
COPY backend_spring/ .

# Cài đặt các phụ thuộc của ứng dụng và build ứng dụng
RUN mvn clean package -DskipTests

# Chạy ứng dụng Spring Boot
CMD ["java", "-jar", "target/backend_spring-0.0.1-SNAPSHOT.jar"]
