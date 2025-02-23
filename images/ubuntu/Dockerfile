FROM ubuntu:20.04

# Update package list
RUN apt-get update

# Install necessary packages
RUN apt-get install -y \
    wget \
    curl \
    ssh \
    rsync \
    openssh-server \
    nano \
    sudo \
    iputils-ping \
    ufw \
    iproute2 \
    lsb-release \
    vim

# Clean up APT when done
RUN apt-get clean

EXPOSE 3306

# Install MySQL Server and Client
RUN apt-get update && apt-get install -y mysql-server mysql-client

# Expose MySQL Port
EXPOSE 3306

# Start MySQL when the container runs
CMD ["bash"]
