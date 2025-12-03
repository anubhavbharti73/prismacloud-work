FROM acpl-os-golden:2025.01 
WORKDIR /app
COPY target/ShopCartH2-0.0.1-SNAPSHOT.jar  /app/app.jar
EXPOSE 1235  
ENTRYPOINT ["java", "-jar", "app.jar"]
