freedomofpress.dockermachine
============================

Installation of docker-machine client, bash completion scripts, and AWS security
group setup.

Requirements
------------

Will need to pip install `boto` if utilizing the custom security group logic for AWS.

Role Variables
--------------

```
docker_machine_version: 0.11.0
docker_machine_url_base: "https://github.com/docker/machine/releases/download/v{{ docker_machine_version }}"
docker_machine_url: "{{docker_machine_url_base}}/docker-machine-{{ansible_system}}-{{ansible_architecture}}"

# dictionary of SHA256 hashes
docker_machine_hashes:
  0.11.0:
    Linux-x86_64: 71de3ce0c2233f9fbc2ca7e359ff29711e3fb078d9c7b808a771a2bcaa24f729
    Linux-armhf: b433390b30aade887fd350b4c3d965c47ae081547625b2b0d9ea1c64f69eacaf
    Linux-aarch64: 91a596e2603fe6f304f809da18011ba1119534aaa2f68d6f26e0b984e2c9ff09
    Darwin-x86_64: 6237c781100adde442419742bae9b0d6816939f95f049690cfef0a34b6f81f97


docker_machine_bash_url: https://raw.githubusercontent.com/docker/machine/master/contrib/completion/bash/docker-machine.bash
# sha256 hash of the bash completion script
docker_machine_bash_hash: 63ec12777671b90340ebe1e692b9adf84fb651e5c752eaf37119fca3b356991f

docker_machine_binary: /usr/local/bin/docker-machine
```


Dependencies
------------

- `marklee77.docker` - https://github.com/marklee77/ansible-role-docker

To-Do
-----
* AWS security-group support

License
-------

MIT

Author Information
------------------

[Freedom of the Press Foundation](https://freedom.press)
