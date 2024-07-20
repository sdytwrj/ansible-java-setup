# ansible-java-setup
This repository contains a GitHub Actions workflow to set up an environment using Docker Compose and Ansible.

## Files
### 'setup.yml'
This is the GitHub Actions workflow configuration file. It sets up Docker Compose to run an Ansible playbook.

### 'playbook.yml'
This is the Ansible playbook file. It updates the apt-get package list and installs the default JDK on an Ubuntu host.

### 'docker-compose.yml'
This is the Docker Compose configuration file. It sets up an Ansible container to run the playbook against an Ubuntu container.

## Usage
To use this workflow:

1.Ensure you have Docker and Docker Compose installed on your runner.
2.Trigger the workflow manually through the GitHub Actions interface.

The workflow will:

1.Check out the repository.
2.Set up Docker Compose.
3.Run the Ansible playbook inside a Docker container.

## Notes
- The setup.yml file is triggered manually using workflow_dispatch.
- The playbook.yml file is mounted into the Ansible container and executed against a local Ubuntu container.
- Adjust the Ansible tasks in playbook.yml as needed for your setup requirements.
