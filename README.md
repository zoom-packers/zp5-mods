# zp5-mods maven

Maven repository for third-party builds that ZP5's mods compile against and that have no official build for Minecraft 26.3. Served from this branch through raw.githubusercontent.com.

| Artifact | Version | Source | Licence |
|---|---|---|---|
| `dev.latvian.mods:kubejs-neoforge` | `26.3-8.1.0-port.1` | [zoom-packers/kubejs @ 26.3](https://github.com/zoom-packers/kubejs/tree/26.3) | LGPL-3.0 |
| `dev.latvian.mods:rhino` | `2603.2.8-port.1` | [zoom-packers/rhino @ 26.3](https://github.com/zoom-packers/rhino/tree/26.3) | MPL-2.0 |

These are unofficial ports, not released or endorsed by the KubeJS team. The jars are byte-identical to the assets of the release [`kubejs-26.3-8.1.0-port.1`](https://github.com/zoom-packers/zp5-mods/releases/tag/kubejs-26.3-8.1.0-port.1).

```groovy
repositories {
    exclusiveContent {
        forRepository {
            maven { url = 'https://raw.githubusercontent.com/zoom-packers/zp5-mods/maven' }
        }
        filter {
            includeModule 'dev.latvian.mods', 'kubejs-neoforge'
            includeModule 'dev.latvian.mods', 'rhino'
        }
    }
}
```

Better Advanced Tooltips, which KubeJS needs at runtime, comes from `https://maven.latvian.dev/releases`.

Never change or delete a published version: builds and packs pin these files by hash. Publish a new version (a new `-port.N` suffix) instead.
