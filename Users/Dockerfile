FROM acpl-os-golden:2025.01
RUN useradd -m appuser
USER appuser
HEALTHCHECK --interval=30s --timeout=3s --retries=3 CMD curl -f http://localhost/health || exit 1
WORKDIR /app
COPY target/Users-0.0.1-SNAPSHOT.jar /app/app.jar	 
EXPOSE 1234
ENTRYPOINT ["java", "-jar", "app.jar"]
