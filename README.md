# ansible-ee

Ansible [Execution Environments](https://ansible.readthedocs.io/en/latest/getting_started_ee/index.html) built with [ansible-builder](https://ansible.readthedocs.io/projects/builder/).

Published to `ghcr.io/stelonld/ansible-ee`.

## Images

| EE | Image | Description |
|---|---|---|
| [iac](iac) | `ghcr.io/stelonld/ansible-ee/iac:latest` | General-purpose IaC EE — ansible-core, ansible-lint, community.general, community.crypto, ansible.posix |

## VS Code

To use an EE with the [VS Code Ansible extension](https://marketplace.visualstudio.com/items?itemName=redhat.ansible), add to `settings.json`:

```json
{
  "ansible.executionEnvironment.enabled": true,
  "ansible.executionEnvironment.image": "ghcr.io/stelonld/ansible-ee/iac:latest",
  "ansible.executionEnvironment.containerEngine": "docker",
  "ansible.executionEnvironment.pull.policy": "missing"
}
```

## ansible-navigator

```yaml
# ansible-navigator.yml
ansible-navigator:
  execution-environment:
    enabled: true
    image: ghcr.io/stelonld/ansible-ee/iac:latest
    pull:
      policy: missing
```
