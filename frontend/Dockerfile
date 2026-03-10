FROM node:22

WORKDIR /app

COPY package*.json ./

RUN npm install

ARG NEXT_PUBLIC_API_KEY
ENV NEXT_PUBLIC_API_KEY=$NEXT_PUBLIC_API_KEY

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]