# Git Sync

This role handles configure git projects using HTTPS and user token.

## Requirements

The hosts you are targeting should have the following packages:

- git
- bash

## Role Variables

| Variable            | Required | Default | Description                                                                                                                                                                                                                                                      |
| ------------------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| git_sync | &#9989;  | `[repo: Repository git, dest: Directory to sync git project, user_login: User to login in git server, token: Git user token, commit_name: Name to configure for commit, commit_email: Email to configure for commit]`    | A list of repositorys to configure.<br><br>|

## Dependencies

None

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - role: luyz25.git_sync
      vars:
        git_sync:
          - repo: github.com/luyz25/git_sync.git
            dest: ~/Documentos/git_sync
            user_login: username
            token: "GIT USER TOKEN"
            commit_name: Luiz Teixeira
            commit_email: luizteixeira@example.com
```

## License

MIT

## Author Information

Luiz Teixeira (@luyz25)
