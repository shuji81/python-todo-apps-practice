# Next.js用 Dockerfile
FROM node:22-alpine

RUN mkdir /frontend
WORKDIR /frontend/app

RUN npm install -g npm@latest && npm install create-next-app
EXPOSE 3000
COPY app/package*.json ./
RUN npm install
COPY app/. . 
CMD ["npm", "run", "dev"]