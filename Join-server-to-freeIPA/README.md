
# Join-server-to-freeIPA

This Ansible suite is designed to automate the process of joining a server to a FreeIPA domain. It includes playbooks and configuration files necessary for setting up and managing this process.

## Table of Contents
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Inventory](#inventory)
- [Playbooks](#playbooks)
- [Roles](#roles)
- [License](#license)

## Project Structure

- `.gitignore`: Specifies files and directories to be ignored by git.
- `inventory.ini.sample`: A sample inventory file.
- `playbook.yml`: The main Ansible playbook for joining a server to FreeIPA.
- `roles/`: Directory containing roles used in the playbook.

## Prerequisites

- Ansible installed on the control machine.
- Access to the target servers with necessary privileges.
- FreeIPA server setup and running.

## Usage

1. **Clone the repository**:
    ```sh
    git clone https://github.com/universcom/Ansible_Automation.git
    cd Ansible_Automation/Join-server-to-freeIPA
    ```

2. **Prepare your inventory file**:
    - Copy the sample inventory file and modify it as needed:
    ```sh
    cp inventory.ini.sample inventory.ini
    ```

3. **Update the inventory file**:
    - Edit `inventory.ini` to include the target hosts and necessary variables.

4. **Run the playbook**:
    - To run the main playbook:
    ```sh
    ansible-playbook -i inventory.ini playbook.yml -e "FREEIPA_PRINCIPAL_USER=<freeIPA admin user>" -e "FREEIPA_PRINCIPAL_PASS=<freeIPA admin password>"
    ```

## Inventory

The `inventory.ini.sample` file provides a template for defining your inventory. Update it with the details of your target servers.

## Playbooks

- `playbook.yml`: The main playbook that automates the process of joining a server to FreeIPA.

## Roles

The `roles/` directory contains roles that are used in the playbooks. Each role is a self-contained unit that can be reused across different playbooks.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
