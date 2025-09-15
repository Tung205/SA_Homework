FROM ubuntu:20.04

# Cài đặt OpenSSH server
RUN apt-get update && apt-get install -y \
    openssh-server sudo nano \
    && mkdir /var/run/sshd \
    && apt-get clean

# Tạo user "docker" với password "docker"
RUN useradd -m -s /bin/bash docker \
    && echo "docker:docker" | chpasswd \
    && adduser docker sudo

# Cho phép SSH login bằng password
RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config \
    && sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config

# Expose port SSH
EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
