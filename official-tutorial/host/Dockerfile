FROM almalinux:latest

RUN dnf update -y && \
	dnf -y install openssh-server passwd && \
	dnf clean all

RUN echo 'root:password' | chpasswd
RUN ssh-keygen -A

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
