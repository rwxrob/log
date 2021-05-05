Wondering what to call my main util for streaming. It was called `live`
before. I think I'll keep that. It was sort of the catch-all for calls
to `twitter` (requires `twurl`), `twitch`, and `yt` API scripts and commands along with
(what are now) aliases to `gh` and the `auth` tool I built to avoid
disconnected tokens. Stuff from `live` applies to all of those services
and orchestrates video updates. I'll have to integrate `zet` and `boost`
now for sure. The `live` tool will have to allow identifying the ZK repo
to which the video belongs. I have several ZK repos at this point (all
managed by the same multicall `zet` script): `zet`, `log`, `boost`,
`lab`, `todo`.
