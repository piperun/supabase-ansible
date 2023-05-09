

Supabase Ansible Role
=========

This Ansible role installs and configures Supabase, an open-source alternative to Firebase, using Docker or Podman.

Requirements
------------

This role requires Docker or Podman to be installed on the target host.

Role Variables
--------------

The following variables can be set to configure Supabase:

| Variable | Default Value | Description |
| -------- | ------------- | ----------- |
| `supabase_version` | `latest` | The version of Supabase to install |
| `supabase_docker_image` | `supabase/supabase` | The Docker or Podman image to use |
| `supabase_env_vars` | `{}` | A dictionary of environment variables to set for Supabase |
| `supabase_ports` | `["5432", "5433", "5434", "80", "443"]` | A list of ports to expose for Supabase |
| `supabase_network` | `"supabase_network"` | The name of the Docker or Podman network to use |

Dependencies
------------

None.

Example Playbook
----------------

Here is an example playbook that installs and configures Supabase:

```
- hosts: servers
  vars:
    supabase_env_vars:
      SUPABASE_KEY: "mysecretkey"
      SUPABASE_URL: "https://mydomain.com"
  roles:
    - role: myuser.supabase
```

License
-------

This role is licensed under the GPL.

Author Information
------------------

Created by [Your Name]. You can reach me at [Your Email Address].