FROM node:16-alpine

# Install git
RUN apk add --no-cache \
  git

# Clone repository
WORKDIR /usr/src/app
RUN git clone https://github.com/sparcs-kaist/taxi-front .

# Install requirements
RUN npm install
RUN npm install serve -g

# Run container
EXPOSE 80
CMD ["sh", "-c", "npm run build && serve -s build -l 80"]
