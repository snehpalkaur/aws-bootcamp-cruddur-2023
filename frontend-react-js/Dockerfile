#FROM node:16.18

#ENV PORT=3000

#COPY . /frontend-react-js
#WORKDIR /frontend-react-js
#RUN npm install
#EXPOSE ${PORT}
#CMD ["npm", "start"]

# Stage 1: Build
FROM node:16.18 AS build
WORKDIR /frontend-react-js
COPY package.json package-lock.json /frontend-react-js/
RUN npm install
COPY . /frontend-react-js
RUN npm run build

# Stage 2: Production
FROM node:16.18
ENV NODE_ENV=production
ENV PORT=3000
WORKDIR /frontend-react-js
COPY package.json package-lock.json /frontend-react-js/
RUN npm install --production
COPY --from=build /frontend-react-js /frontend-react-js
EXPOSE ${PORT}
CMD ["npm", "start"]

