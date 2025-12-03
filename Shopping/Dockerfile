FROM node:18-alpine
WORKDIR /app
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

