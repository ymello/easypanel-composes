# Supabase

- copied from https://github.com/supabase/supabase/tree/master/docker
- removed `container_name`
- removed `ports`


# to install a project in easypanel

```
{
  "services": [
    {
      "type": "compose",
      "data": {
        "serviceName": "supabase-hannah",
        "source": {
          "type": "git",
          "repo": "https://github.com/ymello/easypanel-composes.git",
          "ref": "30-01-2025",
          "rootPath": "/supabase/code",
          "composeFile": "docker-compose.yml"
        },
        "domains": [
          {
            "host": "$(EASYPANEL_DOMAIN)",
            "port": 8000,
            "service": "kong"
          }
        ]
      }
    }
  ]
}

```