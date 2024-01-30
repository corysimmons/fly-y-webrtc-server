# fly-y-webrtc-server

Fly.io WebRTC server for use with y-webrtc.

Launch your own instance because if this one goes down, you're out of luck.

## Getting started

Get a Fly.io account and [install the CLI](https://fly.io/docs/hands-on/install-flyctl/).

- `git clone git@github.com:corysimmons/fly-y-webrtc-server.git`
- `cd fly-y-webrtc-server`
- `fly launch`
- `fly deploy`

If it doesn't work because of an app name conflict, you can probably just change this line in `fly.toml`:

```toml
app = 'fly-y-webrtc-server-<your-name-here>'
```

Now you should be able to use this server in your y-webrtc app like so:

```ts
new WebrtcProvider('your-room-name', ydoc, {
  signaling: ['wss://fly-y-webrtc-server.fly.dev'],
})
```

I'm new to all this stuff so if you have any issues, please open an issue or PR. Thanks!
