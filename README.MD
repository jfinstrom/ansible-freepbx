# FreePBX 17 Ansible Playbook for Debian 12

This Ansible playbook automates the installation of FreePBX 17 on a clean Debian 12 build, including the compilation of Asterisk from source.

## Usage

1. Clone the repository:

    ```bash
    git clone https://github.com/jfinstrom/ansible-freepbx.git
    cd ansible-freepbx
    ```

2. Edit configuration files:

    - Adjust the Asterisk version in `playbooks/Debian-FreePBX17/vars/versions.yml`:

        ```yaml
        asterisk_version: 20.5.0
        ```

    - Copy and edit the user information in `playbooks/Debian-FreePBX17/vars/user_info.yml`:

        ```yaml
        developer: true
        github_username: "your-github-username"
        git_user_name: "Your Full Name"
        git_user_email: "your.email@example.com"
        ```

3. Run the playbook:

    ```bash
    ansible-playbook playbooks/Debian-FreePBX17/freepbx17.yml -i inventory/servers --ask-pass
    ```

## Configuration Files

### `vars/versions.yml`

This file contains the version information for Asterisk. Adjust the `asterisk_version` variable as needed.

### `vars/user_info.yml`

Copy this file from `vars/user_info.yml.sample` and provide the required information:

```yaml
developer: true
github_username: "your-github-username"
git_user_name: "Your Full Name"
git_user_email: "your.email@example.com"
```

## License

This project is licensed under the [MIT License](LICENSE).
