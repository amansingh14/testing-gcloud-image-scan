# Use an old Ubuntu release (has known CVEs)
FROM ubuntu:18.04

# Set a maintainer label
LABEL maintainer="test@example.com"

# Install outdated packages (intentionally vulnerable)
RUN apt-get update && \
    apt-get install -y \
        curl \
        python


# Add a vulnerable application (optional)
RUN curl -o /tmp/vuln-app.sh https://raw.githubusercontent.com/vulhub/vulhub/master/test-scripts/test.sh \
    && chmod +x /tmp/vuln-app.sh

# Default command
CMD ["bash"]
