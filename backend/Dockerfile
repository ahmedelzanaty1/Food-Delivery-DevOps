# Base Image
FROM node:18-alpine

# work Directory
WORKDIR /app
# package.json and package-lock.json copy

COPY package*.json ./

# install dependencies
RUN npm install --production

#copy all files
COPY . .

#wxpose port
EXPOSE 4000

#start command
CMD ["npm", "start"]
