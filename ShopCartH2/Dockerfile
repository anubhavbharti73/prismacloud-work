FROM acpl-os-golden:2025.01 
HEALTHCHECK --interval=30s --timeout=3s --retries=3 CMD curl -f http://localhost/health || exit 1
RUN useradd -m appuser
USER appuser
WORKDIR /app
COPY target/ShopCartH2-0.0.1-SNAPSHOT.jar  /app/app.jar
EXPOSE 1235  
ENTRYPOINT ["java", "-jar", "app.jar"]
