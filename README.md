## Running the Playbook

To execute the playbook, run the following command:

```bash
ansible-playbook -i inventory.ini setup.yml --ask-become-pass
```

This will run the **base**, **nginx**, **app**, and **ssh** roles in sequence. The `--ask-become-pass` flag prompts you for a password to execute tasks with sudo privileges.

### Running Specific Roles

If you want to run only specific roles, you can use the `--tags` option. For example, to run only the **app** role:

```bash
ansible-playbook -i inventory.ini setup.yml --tags "app"
```

