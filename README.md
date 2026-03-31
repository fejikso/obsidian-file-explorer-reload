# File Explorer Reload

[![GitHub release](https://img.shields.io/github/v/release/fejikso/obsidian-file-explorer-reload)](https://github.com/fejikso/obsidian-file-explorer-reload/releases)
[![GitHub downloads](https://img.shields.io/github/downloads/fejikso/obsidian-file-explorer-reload/total)](https://github.com/fejikso/obsidian-file-explorer-reload/releases)

> **Fork notice**: This repository is a fork of [mnaoumov/obsidian-file-explorer-reload](https://github.com/mnaoumov/obsidian-file-explorer-reload).
> The upstream project is authored by **Michael Naumov**; this fork is maintained by **fejikso**.

This is a plugin for [Obsidian](https://obsidian.md/) that reloads the file explorer files list.

It is needed sometimes when you made a bulk file operation (copy / move / delete) outside of `Obsidian` while it is open and some of those changes aren't reflected in the `File Explorer` pane. So you might see in the `File Explorer` some files that don't actually exist in the file system, or the opposite, you might miss some files that actually exist in the file system.

- [Video of the issue](https://www.youtube.com/watch?v=C-uKULzPNX4).
- Discussion on the [Official Obsidian forum].

The usual workaround for this problem is to close and reopen `Obsidian` or invoke `Reload app without saving` command, but for big vaults such workarounds adds undesired waiting time, which the current plugin is aiming to avoid.

The plugin adds `Reload File Explorer` command, `Reload Folder` and `Reload Folder with Subfolders` context menu items.

## This fork

- **Maintainer**: [fejikso](https://github.com/fejikso)
- **Scope**: personal build with minor tweaks
- **Notable differences**:
  - Adds a ribbon “refresh” button to reload the file tree (reloads the active file’s parent folder when possible; otherwise reloads the whole tree)

Also you can use this plugin's functionality programmatically

```js
await app.plugins.plugins['file-explorer-reload'].reloadDirectory(
  directoryPath,
  isRecursive
);
```

## Upstream / Credits

- **Upstream author**: [Michael Naumov](https://github.com/mnaoumov/)
- **Upstream repository**: [mnaoumov/obsidian-file-explorer-reload](https://github.com/mnaoumov/obsidian-file-explorer-reload)

## Installation

The plugin is not available on [the official Community Plugins repository](https://obsidian.md/plugins) yet.

The Obsidian team [decided](https://github.com/obsidianmd/obsidian-releases/pull/2783#issuecomment-1936153306) to not accept this plugin to the repository.

If you want to bring Obsidian team's attention to the problem solved by this plugin, you can leave a comment in the [Official Obsidian forum].

### Beta versions

To install the latest beta release of this plugin (regardless if it is available in [the official Community Plugins repository](https://obsidian.md/plugins) or not), follow these steps:

1. Ensure you have the [BRAT plugin](https://obsidian.md/plugins?id=obsidian42-brat) installed and enabled.
2. Click [Install via BRAT](https://intradeus.github.io/http-protocol-redirector?r=obsidian://brat?plugin=https://github.com/fejikso/obsidian-file-explorer-reload).
3. An Obsidian pop-up window should appear. In the window, click the `Add plugin` button once and wait a few seconds for the plugin to install.

## Debugging

By default, debug messages for this plugin are hidden.

To show them, run the following command:

```js
window.DEBUG.enable('file-explorer-reload');
```

For more details, refer to the [documentation](https://github.com/mnaoumov/obsidian-dev-utils/blob/main/docs/debugging.md).

## Support

<!-- markdownlint-disable MD033 -->

If you’d like to support the upstream author, please see the upstream repository.

<!-- markdownlint-enable MD033 -->

## My other Obsidian resources

Upstream: [mnaoumov/obsidian-resources](https://github.com/mnaoumov/obsidian-resources).

## License

© [Michael Naumov](https://github.com/mnaoumov/)

[Official Obsidian forum]: https://forum.obsidian.md/t/sometimes-changes-made-outside-of-obsidian-are-not-reflected-in-the-files-pane/73451
