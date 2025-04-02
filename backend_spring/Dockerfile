# 1️⃣ Sử dụng Maven image để build app
FROM maven:3.9.6-eclipse-temurin-21 AS builder
WORKDIR /app

# Copy pom.xml trước để cache dependencies
COPY backend_spring/pom.xml ./
RUN mvn dependency:go-offline

# Copy toàn bộ source code và build
COPY backend_spring/. ./
RUN mvn clean package -DskipTests

# 2️⃣ Sử dụng JDK nhẹ để chạy ứng dụng
FROM eclipse-temurin:21-jdk
WORKDIR /app

# Copy file .jar đã build từ bước trước
COPY --from=builder /backend_spring/target/backend_spring-0.0.1-SNAPSHOT.jar app.jar


# Chạy ứng dụng
CMD ["java", "-jar", "app.jar"]
