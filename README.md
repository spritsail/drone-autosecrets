# drone-autosecrets

This simple script takes constant secret values from a pass entry and sets them on a Drone CI repository. It was written for our use so is not very general.

It assumes the use of [pass](https://git.zx2c4.com/password-store) with an entry named `drone.spritsail.io/env` (this should be adapted to your needs)
This tool makes the use of the [drone cli](https://github.com/drone/cli) for communicating with the Drone server so ensure that it is configured correctly.

If the repository has a valid microbadger repository, it will add the webhook token too.

## Usage

```sh
drone-secrets <user/repo> [-t,--trusted]
```

- `-t`, `--trusted` sets the repository to trusted
