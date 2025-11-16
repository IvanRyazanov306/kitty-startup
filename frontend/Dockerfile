FROM node:20

WORKDIR /app

# package.json содержит зависимости (express, jade, typescript и т.п.)
COPY package.json ./
COPY tsconfig.json ./
COPY frontend.ts ./
COPY index.jade ./

RUN npm install

# собираем TypeScript в JavaScript
RUN npm run build

# после сборки рядом появится frontend.js
CMD ["node", "frontend.js"]