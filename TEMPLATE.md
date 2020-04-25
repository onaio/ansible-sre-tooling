## Ansible Role Template

This is a repository template for Ansible roles. See GitHub's documentation on how to [create a repository from a template](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).

This template runs tests using Ansible Molecule. Automated tests have been configured to run on GitHub actions in the [.github/workflows/ci.yml](.github/workflows/ci.yml) file. The Docker Molecule driver is used to run the tests. The following pip packages are required (if you were to run Ansible Molecule locally):

1. molecule
1. docker-py

After you create your repository from this template:

1. Replace all occurrences of "ansible-role" with the name of your role. If your role is, for instance, called "ansible-superset", make the change using `find . -type f | xargs sed -i  's/ansible-role/ansible-superset/g'`.
1. Set the `ansible_galaxy_api_key` secret in your repository's settings to enable publishing tags to Ansible Galaxy.
1. Update the owner and date in the [LICENSE](./LICENSE) file.
