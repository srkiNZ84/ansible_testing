# Ansible Testing Demo

Demo repository to document layout of an Ansible playbook with roles that have "testing" tasks, which can be run independently of the main playbook run.

## How to use
Run everything (main tasks and tests):
```ansible-playbook -i hosts smoke_test.yml```

Run only tests:
```ansible-playbook -i hosts smoke_test.yml -t smoketests```

Run role A main tasks and tests:
```ansible-playbook -i hosts smoke_test.yml -t aardvark```

Run tests only for role A:
```ansible-playbook -i hosts smoke_test.yml -t aardvark,smoketests --skip-tags bison,caribou```

