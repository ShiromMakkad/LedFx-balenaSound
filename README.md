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

## Other notes

- By default, this deploys the dev branch of LedFx. The maintainers of LedFx recommend the dev branch, but it can be a little less stable, so if you're having issues, you can change it in the `docker-compose.yml`. Just change the tag on `shirom/ledfx:dev` to `shirom/ledfx`.

## Configuration

See [balenaSound customization](https://sound.balenalabs.io/docs/customization)
