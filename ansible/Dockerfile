FROM ansible/centos7-ansible

# Add playbooks to the Docker image
ADD sample /srv/example/
WORKDIR /srv/example

# Run Ansible to configure the Docker image
RUN ansible-playbook site.yml -c local

# Other Dockerfile directives are still valid
EXPOSE 22 3000 80
ENTRYPOINT ["/usr/local/bin/apachectl", "-DFOREGROUND"]
