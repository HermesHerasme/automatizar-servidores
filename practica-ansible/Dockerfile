FROM ubuntu:22.04

RUN apt update && apt install -y openssh-server sudo && \
    useradd -m ansible && echo 'ansible:ansible' | chpasswd && \
    usermod -aG sudo ansible && \
    echo 'ansible ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers && \
    mkdir /var/run/sshd

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
