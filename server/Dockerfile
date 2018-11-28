FROM node:alpine
WORKDIR /usr/apps/fib-cal-aws/server
COPY ./package.json ./
RUN npm install
COPY ./ ./
CMD ["npm" , "run", "start"]