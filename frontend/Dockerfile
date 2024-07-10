# Stage 1: Build the React app
# FROM node:16-alpine AS build
FROM node:lts AS development

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# build the application
RUN npm run build


EXPOSE 5173


# Run the development server on container start
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
