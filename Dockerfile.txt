FROM httpd:2.4

# Copy website files
COPY index.html /usr/local/apache2/htdocs/

# Expose Apache port
EXPOSE 80

# Add labels (useful for Prometheus later)
LABEL app="apache-web"
LABEL environment="dev"
