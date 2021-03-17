# LedFx-balenaSound
[LedFx](https://github.com/LedFx/LedFx) and [balenaSound](https://github.com/balenalabs/balena-sound) With One Click!

## Deployment

Just click the button to deploy it!

[![balena deploy button](https://www.balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/ShiromMakkad/LedFx-balenaSound)

You can also clone the repository and use `balena push` to deploy your code with any changes. 

## Hardware Requirements

Minimum Required: Raspberry Pi 3B+

**Strongly** recommended: Raspberry Pi 4

Both balenaSound and LedFx alone have minimum requirements at the 3B+, and balenaSound alone still has issues on the 3B+. It's possible to run them both on a 3B+, but it has significant lag. 

## Note:

- The UPNP reciever is extremely buggy. See [balena/balena-sound#342](https://github.com/balenalabs/balena-sound/issues/342). This issue can also prevent other recievers from getting audio even after you've restarted the UPNP container, and there's no error logging to go with it. If you're not using UPNP, I strongly recommend disabling it to prevent it from interfering with the rest of the audio system. You can do this by adding the `SOUND_DISABLE_UPNP` environment variable in Balena after you deploy it. See [Configuration](#configuration).
- Typically, LedFx will run on port `8888`, but this container runs on port `80`. This is done to take advantage of Balena's public device URL feature, but you should keep that change in mind when connecting using a browser. You can change this behavior in the `docker-compose.yml` by changing the line `80:8888` to `8888:8888`. 

## Configuration

See [balenaSound customization](https://sound.balenalabs.io/docs/customization)
