FROM ubuntu:20.04

WORKDIR /app

RUN apt-get update && apt-get install -y \
    python3-pip \
    python3-dev \
    build-essential \
    curl

# Install Next.js
RUN npm install -g next react react-dom

# Install MongoDB
RUN apt-get install -y mongodb

# Install Django
RUN pip3 install django

COPY . /app

EXPOSE 3000

EXPOSE 8000

CMD ["npm", "run", "dev"]
