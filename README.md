
This script polls the state of build pipelines in GoCD.  If a GoCD build fails,
it connects to a Vera (home automation system) and calls a scene (to e.g.
turn the alarm lights on).

It needs two configuration files:

1) `gocd.cfg` - defines GoCD parameters and the Vera Scene name to call when
the build has failed.

```
{
  "server": "https://gocd.myenterprise.com:8154",
  "username": "my-user",
  "password": "my-password",
  "scene": "Red",
}
```

2) `vera.cfg` - defines Vera location and authentication

```
{
  "remote": {
    "user": "vera-user",
    "password": "vera-password",
    "device": "98765131924"
  }
}
```

