# passgen

This Ansible playbook generates unique random passwords for the user of choice on multiple hosts, updates its password, and stores the generated passwords in a file on the Ansible control machine.

## Requirements

- Ansible installed on the control machine.
- `passlib` library installed on the control machine. You can install it using pip:
  ```sh
  pip install passlib
  ```

## Variables

- `user`: The username for which the password will be changed. Default is root.
- `password_length`: The length of the generated passwords. Default is 16.
- `password_chars`: The character sets used for generating the passwords. Default is "ascii_letters,digits,punctuation".
- `password_file`: The file path on the control machine where the passwords will be stored.

## Running the playbook

Create an inventory file named `hosts.ini` with the details of your hosts and run the playbook using the following command:

```sh
ansible-playbook -i hosts.ini change_user_password.yml
```
