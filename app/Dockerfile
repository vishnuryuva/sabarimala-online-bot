FROM mcr.microsoft.com/playwright:v1.56.1-jammy
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
ENV PORT=3000 HOST=0.0.0.0
EXPOSE 3000
# Node itself is capped at 192 MB so the memory stays for the browser sessions.
CMD ["node", "--max-old-space-size=192", "server.js"]
