# Background

We observed some failing tasks in our ansible setup due to variables that
should not be defined. After some debugging, we figured out that variables
defined in a role can leek into earlier roles in the same play (meaning
"section" in playbook starting
with `- hosts: ...`).

We observed this with ansible 2.5.2.

# Usage

Just run

```
ansible-playbook site.yml
```
