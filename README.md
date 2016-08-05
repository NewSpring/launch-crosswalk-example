# Launch Crosswalk Example

[![Build Status](https://travis-ci.org/NewSpring/launch-crosswalk-example.svg?branch=master)](https://travis-ci.org/NewSpring/launch-crosswalk-example)

1. [Build on Travis](https://travis-ci.org/NewSpring/launch-crosswalk-example)
2. [Site on Heroku](https://launch-crosswalk-example.herokuapp.com/)
3. [App download on Hockey](https://rink.hockeyapp.net/apps/b8ce93866d44406d950cf9a390b235e1)

## launch.json

```json
{
  "ANDROID_STORE_PASS": "password",
  "ANDROID_KEY": "launch-basic-example",
  "ANDROID_ZIPALIGN": "path/to/zipalign",
  "ANDROID_HOCKEY_TOKEN": "token",
  "ANDROID_HOCKEY_ID": "id",
  "GALAXY_DEPLOY_HOSTNAME": "galaxy.meteor.com",
  "GALAXY_SESSION_FILE": "deployment_token.json",
  "PLAY_AUTH_FILE": "google-auth.json"
}
```

## launch commands

```shell
$ launch galaxy launch-crosswalk-example.meteorapp.com
$ launch build launch-crosswalk-example.meteor.com
$ launch hockey
```

## Secrets

```
tar cvf secrets.tar launch.json .keystore deployment_token.json
travis encrypt-file secrets.tar .travis/secrets.tar.enc
```

