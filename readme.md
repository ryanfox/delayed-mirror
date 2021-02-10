# Semi-Instant Replay

Plays continuous video from a camera, on a delay. It's useful for (for example) checking your form after a set in the gym. Or anything you can't look away from in the moment, but want to see after the fact.

You'll need:

- A Raspberry Pi with Raspbian installed and an HDMI output
- 1 official Pi camera
- An HDMI cable
- A screen to display it on.


## Setup

Semi-Instant Replay depends on VLC. Install with `sudo apt install vlc`.


## Running the replay

Start the server in the background with

```
$ sh ./server.sh &
```

Once that is running, start the client:

```
$ sh ./client.sh
```

Plug in the HDMI cable, and you're up and running! Well, in the future anyway.


If you want to change the delay, set `--sout-rtp-caching` in `server.sh` to the value you want, in milliseconds. The longer the delay, the more memory it will use, so at some point the RAM on your Pi will cap it.

