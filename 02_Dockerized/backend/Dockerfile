FROM node:14.15.0
WORKDIR /app
COPY ["package.json", "package-lock.json", "wait-for.sh", "startup.sh", "./"]
RUN ["apt-get","update","&&","apt-get","install","netcat","-y"] 
RUN ["chmod","+x","./wait-for.sh","./startup.sh"]
RUN npm install --production
COPY . .
EXPOSE 5000
CMD ["npm", "start"]
