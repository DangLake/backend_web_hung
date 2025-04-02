# Sử dụng JDK 21
FROM eclipse-temurin:21-jdk

# Đặt thư mục làm việc trong container
WORKDIR /app

# Copy tất cả mã nguồn vào container
COPY . .

# Cài đặt các phụ thuộc của ứng dụng
RUN mvn clean package -DskipTests

# Chạy ứng dụng Spring Boot
CMD ["java", "-jar", "target/backend_spring-0.0.1-SNAPSHOT.jar"]
