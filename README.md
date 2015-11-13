# Ansible Testing Demo

Demo repository to document layout of an Ansible playbook with roles that have "testing" tasks, which can be run independently of the main playbook run.

Read more about it here: https://blog.dukic.co.nz/index.php/2015/11/13/ansible-strategy-for-including-smoke-tests/

## How to use
Run everything (main tasks and tests):
```ansible-playbook -i hosts smoke_test.yml```

Run only tests:
```ansible-playbook -i hosts smoke_test.yml -t smoketests```

Run role A main tasks and tests:
```ansible-playbook -i hosts smoke_test.yml -t aardvark```

Run tests only for role A:
```ansible-playbook -i hosts smoke_test.yml -t role_a_smoketest```

Or:

```ansible-playbook -i hosts smoke_test.yml -t smoketests --skip-tags bison,caribou```
second way is not ideal, as you have to know the full list of tags to skip.
