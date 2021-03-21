# Meet

This stack features the basic video solution using Jitsi Meet.

## Requirements

- Docker and Docker Compose
- Git (optional)

## Setting the conditions

➊ Download the project

```bash
git clone https://github.com/fonoster/meet
```

➋  Create required CONFIG directories

```bash
mkdir -p ~/.jitsi-meet-cfg/{config/jitsi,etc,web/letsencrypt,transcripts,prosody/config,prosody/prosody-plugins-custom,jicofo,jvb,jigasi,jibri}
```

For Windows: 

```bash
echo config/jitsi,etc,web/letsencrypt,transcripts,prosody/config,prosody/prosody-plugins-custom,jicofo,jvb,jigasi,jibri | % { mkdir "~/.jitsi-meet-cfg/$_" }
```

➌ Copy the example enviroment file `env_example` into `.env` and then update the variables `DOCKER_HOST_ADDRESS` and `CONFIG` to reflect your environment.

## Running the stack

Run the stack with the following command:

```bash
docker-compose -f docker-compose.yml up
```

