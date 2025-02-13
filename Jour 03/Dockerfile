FROM nginx:latest

# Set working directory inside container
WORKDIR /usr/share/nginx/html

# Copy static files (index.html)
COPY index.html .

# Create a directory for storing game results
RUN mkdir -p /usr/share/nginx/html/game-results

# Copy files that should be persistent in the volume
COPY save.php /usr/share/nginx/html/game-results/
COPY results.json /usr/share/nginx/html/game-results/

# Define a volume to persist game results
VOLUME ["/usr/share/nginx/html/game-results"]

# Expose port 80 inside the container
EXPOSE 80
