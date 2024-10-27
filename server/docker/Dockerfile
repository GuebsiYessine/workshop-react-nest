FROM node:21 
#directory mt3 el work fl container
WORKDIR /app

ENV DATABASE_URL=$DATABASE_URL

#first step
COPY ./package*.json ./
COPY ./tsconfig.json ./

RUN npm install 
COPY ./ ./ 

RUN npm run build 

RUN npx prisma generate

CMD [ "npm", "run", "start:dev" ]