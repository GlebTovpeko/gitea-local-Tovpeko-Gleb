# gitea-local

В корне проекта создать папку .data

В ней создать две папки:
   - gitea
   - runner

В файл /etc/host (или C:\Windows\System32\drivers\etc\hosts)

добавить запись:

127.0.0.1       git.sirius.local

Добавить в конфигурационный файл Docker'a слудующую запись:

```json
{
   ...
  "insecure-registries" : [
    "host.docker.internal:3000"
  ]
  ...
}
```

Конфиг Docker'a искать здесь:
   - Linux: /etc/docker/daemon.json
   - Windows: C:\ProgramData\docker\config\daemon.json