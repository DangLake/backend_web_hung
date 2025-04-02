# Sử dụng JDK 21
FROM eclipse-temurin:21-jdk

# Đặt thư mục làm việc trong container
WORKDIR /app

# Copy file JAR vào container
COPY target/*.jar app.jar

# Chạy ứng dụng Spring Boot
CMD ["java", "-jar", "app.jar"]
