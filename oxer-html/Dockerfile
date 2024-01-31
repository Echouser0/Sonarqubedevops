FROM openjdk:11-jre

WORKDIR /app

# Install necessary tools
RUN apt-get update && \
    sudo apt-get install -y wget unzip

# Download and install Checkmarx CLI
RUN wget https://github.com/Checkmarx/ast-cli/releases/download/2.0.63/ast-cli_linux_x64.tar.gz
    tar -xzf ast-cli_linux_x64.tar.gz
    ./cx

# Set environment variables
ENV PATH="/app/checkmarx:${PATH}"

CMD ["bash"]
