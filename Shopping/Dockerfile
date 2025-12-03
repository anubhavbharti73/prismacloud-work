FROM node:18-alpine
RUN useradd -m appuser
USER appuser
WORKDIR /app
HEALTHCHECK --interval=30s --timeout=3s --retries=3 CMD curl -f http://localhost/health || exit 1
# Clean npm cache to avoid idealTree error
RUN npm cache clean --force
COPY package*.json ./
# Install local dependencies first
RUN npm install
# Then install Angular CLI
RUN npm install -g @angular/cli
COPY . .
EXPOSE 4200
CMD ["ng", "serve", "--host", "0.0.0.0"]

