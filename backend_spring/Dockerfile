# Sử dụng JDK 21 làm base image
FROM eclipse-temurin:21-jdk

# Đặt thư mục làm việc trong container
WORKDIR /app

# Sao chép file .jar vào container
COPY target/backend_spring-0.0.1-SNAPSHOT.jar app.jar


# Chạy ứng dụng Spring Boot
CMD ["java", "-jar", "app.jar"]
