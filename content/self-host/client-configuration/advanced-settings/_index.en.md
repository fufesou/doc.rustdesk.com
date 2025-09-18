---
title: Advanced Settings
weight: 49
---

All advanced settings in custom clients are covered here.

## Privilege Levels for Settings

There are four types of settings:

1. Override settings, in `Web Console` → `Custom Clients`
2. Default settings, in `Web Console` → `Custom Clients`
3. User settings, in the RustDesk client
4. Strategy settings, in `Web Console` → `Strategies`

The hierarchy of privilege for these settings is as follows: `Override > Strategy > User > Default`.

## Security Settings

### access-mode

Set the access mode (permissions) for incoming connections.

**Location**:

1. **Desktop** Settings → Security → Permissions
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | custom, full, view | custom | `access-mode=custom` |

### enable-keyboard

Enable keyboard/mouse input for incoming connections.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable keyboard
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-keyboard=Y` |

### enable-clipboard

Enable copy and paste for incoming connections.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable clipboard
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-clipboard=Y` |

### enable-file-transfer

Enable file copy and paste or file transfer (session) for incoming connections.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable file transfer
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-file-transfer=Y` |


### enable-camera

Enable camera for incoming connections.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable camera
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-camera=Y` |

### enable-terminal

Enable terminal for incoming connections.

**Location**:

**Desktop** Settings → Security → Permissions → Enable terminal

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-terminal=Y` |

### enable-remote-printer

Enable remote printer for incoming connections.

**Location**:

1. **Windows** Settings → Security → Permissions → Enable remote printer

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-remote-printer=Y` |

### enable-audio

Enable audio record and transfer to peer.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable audio
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-audio=Y` |

### enable-tunnel

Enable TCP tunneling.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable TCP tunneling
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-tunnel=Y` |

### enable-remote-restart

Enable restarting by the control side.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable remote restart
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-remote-restart=Y` |

### enable-record-session

Enable sessions to be recorded.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable recording session
2. **Mobile** Settings → Share screen → Enable recording session

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-record-session=Y` |

### enable-block-input

Enable the control side to block other users' input.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable blocking user input (Windows only)
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-block-input=Y` |

### allow-remote-config-modification

Allow the control side to change the settings in controlled RustDesk UI.

**Location**:

1. **Desktop** Settings → Security → Permissions → Enable remote configuration modification
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `allow-remote-config-modification=Y` |

### enable-lan-discovery

Allows LAN peers to discover me.

After LAN discovery, [WOL](https://en.wikipedia.org/wiki/Wake-on-LAN) can work if supported locally.

**Location**:

1. **Desktop** Settings → Security → Security → Deny LAN discovery
2. **Mobile** Settings → Share screen → Deny LAN discovery

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| Y | Y, N | Y | `enable-lan-discovery=Y` |

### direct-server

Enable direct IP access.

**Location**:

1. **Desktop** Settings → Security → Security → Enable direct IP access
2. **Mobile** Settings → Share screen → Direct IP access

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `direct-server=Y` |

### direct-access-port

Direct IP access port.

**Location**:

1. **Desktop** Settings → Security → Security → Direct IP access port (Show if "Enable direct IP access" is checked)
2. **Mobile** Settings → Share screen → Direct IP access

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N |  | 21118 | `direct-access-port=21118` |

### whitelist

Use IP Whitelisting.

**Location**:

1. **Desktop** Settings → Security → Security → Use IP Whitelisting
2. **Mobile** Settings → Share screen → Use IP Whitelisting

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | `,` or `<ip1>,<ip2>,<ip3>` | `,` means no filter | `whitelist=,` |

### allow-auto-disconnect & auto-disconnect-timeout

Automatically close incoming sessions after a period of user inactivity.

**Location**:

1. **Desktop** Settings → Security → Security → Automatically close incoming sessions on user inactivity
2. **Mobile** Settings → Share screen → Automatically close incoming sessions on user inactivity

| Option | Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: | :------: |
| allow-auto-disconnect | N | Y, N | N | `allow-auto-disconnect=Y` |
| auto-disconnect-timeout | N | Timeout in minutes | 10 | `auto-disconnect-timeout=10` |

### allow-only-conn-window-open

Only allow connection if RustDesk window is open.

**Location**:

1. **Desktop** Settings → Security → Security → Only allow connection if RustDesk window is open
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| Y | Y, N | N | `allow-only-conn-window-open=N` |

### approve-mode

Accept incoming connections via password or manually click.

**Location**:

1. **Desktop** Settings → Security → Password → Dropdown box
2. **Mobile** Share screen → Dropdown menu on right-up corner

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | password, click, password-click | password-click | `approve-mode=password-click` |

### verification-method

What type of password can be used, `temporary password` refers to the one-time random password.

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | use-temporary-password, use-permanent-password, use-both-passwords | use-both-passwords | `verification-method=use-permanent-password` |

### temporary-password-length

1. **Desktop** Settings → Security → Password → One-time password length
2. **Mobile** Share screen → Dropdown menu on right-up corner → One-time password length

The length of the temporary password.

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | 6, 8, 10 | `temporary-password-length=6` |

### proxy-url

The proxy URL.

Currently support `http` and `socks5`.

**Location**:

1. **Desktop** Settings → Network → Proxy → Socks5/Http(s) proxy
2. **Mobile**

Examples:

1. **http** `proxy-url=http://192.168.0.2:12345`
2. **https** `proxy-url=https://192.168.0.2:12345`
3. **socks5** `proxy-url=socks5://192.168.0.2:1080`

### proxy-username & proxy-password

Proxy username and password.

**Location**:

1. **Desktop** Settings → Network → Proxy → Socks5/Http(s) proxy
2. **Mobile**

| Option | Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: | :------: |
| proxy-username | N | | | `proxy-username=user` |
| proxy-password | N | | | `proxy-password=pass` |

## General Settings

### theme

Controls the UI theme of RustDesk client.

**Location**:

1. **Desktop** Settings → General → Theme
2. **Mobile** Settings → Settings → Theme

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | dark, light, system | system | `theme=system` |

### lang

Controls the language of RustDesk client.

**Location**:

1. **Desktop** Settings → General → Language
2. **Mobile** Settings → Settings → Language

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | default, ar, bg, ... | default | `lang=default` |

Currently available languages are:

ar, bg, ca, cs, da, de, el, en, eo, es, et, fa, fr, he, hr, hu, id, it, ja, ko, kz, lt, lv, nb, nl, pl, pt, ro, ru, sk, sl, sq, sr, sv, th, tr, uk, vn, zh-cn, zh-tw

You can check [LANGS](https://github.com/rustdesk/rustdesk/blob/master/src/lang.rs#L45) in the code for the latest language list.

### allow-auto-record-incoming

Automatically record incoming sessions.

**Location**:

1. **Desktop** Settings → General → Recording → Automatically record incoming sessions
2. **Mobile** Settings → Recording → Automatically record incoming sessions

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `allow-auto-record-incoming=Y` |

### allow-auto-record-outgoing

Automatically record outgoing sessions.

**Location**:

1. **Desktop** Settings → General → Recording → Automatically record outgoing sessions
2. **Mobile** Settings → Recording → Automatically record outgoing sessions

| Install required | Values | Default | Example | Version |
| :------: | :------: | :------: | :------: | :------: |
| N | Y, N | N | `allow-auto-record-outgoing=Y` | >= 1.3.2 |

### video-save-directory

The directory to save recorded videos.

**Location**:

1. **Desktop** Settings → General → Recording → Video save directory
2. **Mobile** Settings → Recording

Default values:

1. **macOS** ~/Movies/**app_name**
2. **Linux** ~/Videos/**app_name**
3. **Windows** %USERPROFILE%\Videos\\**app_name**
4. **Android** /Storage/emulated/0/**app_name**/ScreenRecord

**Note**: Replace **app_name** means current app name.

### enable-confirm-closing-tabs

Controls whether to show a confirm dialog before closing all remote tabs.

**Location**:

1. **Desktop** Settings → General → Other → Confirm before closing multiple tabs
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-confirm-closing-tabs=Y` |

### enable-abr

Enable adaptive bitrate.

**Location**:

1. **Desktop** Settings → General → Other → Adaptive bitrate
2. **Mobile** Settings → Share screen → Adaptive bitrate (beta)

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-abr=Y` |

### allow-remove-wallpaper

Remove wallpaper during incoming sessions.

**Location**:

1. **Desktop** Settings → General → Other → Remove wallpaper during incoming sessions
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `allow-remove-wallpaper=N` |

### enable-open-new-connections-in-tabs

Controls whether to use a new tab or a new window to open a new connection.

**Location**:

1. **Desktop** Settings → General → Other → Open connection in new tab
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-open-new-connections-in-tabs=Y` |

### allow-always-software-render

Always use software rendering.

**Location**:

1. **Desktop** Settings → General → Other → Always use software rendering
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `allow-always-software-render=N` |

### allow-linux-headless

Allow incoming connection if there's no displays.

This option requires desktop environment, Xorg server and GDM, see [PR 3902](https://github.com/rustdesk/rustdesk/pull/3902).

**Location**:

1. **Desktop** Settings → General → Other → Allow Linux headless
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| Y | Y, N | N | `allow-linux-headless=N` |

### enable-hwcodec

Enable hardware encoding to make the picture smoother.

**Location**:

1. **Desktop**
2. **Mobile** Settings → Hardware codec

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | Y | `enable-hwcodec=Y` |

### peer-card-ui-type

Controls the view of peer cards, includes "Big tiles", "Small tiles" and "List".

**Location**:

1. **Desktop** Home → Peer panel → Right top grid icon
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | 0, 1, 2 | 0 | `peer-card-ui-type=0` |

**0** Big tiles  
**1** Small tiles  
**2** List

### peer-sorting

Controls the ordering of peer cards.

**Location**:

1. **Desktop** Home → Peer panel → Right top sort icon
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Remote ID, Remote Host, Username | Remote ID | `peer-sorting=Remote ID` |

### sync-ab-with-recent-sessions

Controls whether to sync the address book with recent sessions.

**Location**:

1. **Desktop** Home → Peer panel → Address book → Tags → Dropdown menu → Sync with recent sessions
2. **Mobile** Home → Peer panel → Address book → Tags → Dropdown menu → Sync with recent sessions

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `sync-ab-with-recent-sessions=N` |

### sync-ab-tags

Controls whether to sort the address book tags.

**Location**:

1. **Desktop** Home → Peer panel → Address book → Tags → Dropdown menu → Sort tags
2. **Mobile** Home → Peer panel → Address book → Tags → Dropdown menu → Sort tags

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `sync-ab-tags=N` |

### filter-ab-by-intersection

Filter address book by tag intersection.

**Preview**: [PR #5985](https://github.com/rustdesk/rustdesk/pull/5985)

**Location**:

1. **Desktop** Home → Peer panel → Address book → Tags → Dropdown menu → Filter by intersection
2. **Mobile** Home → Peer panel → Address book → Tags → Dropdown menu → Filter by intersection

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `filter-ab-by-intersection=N` |

### use-texture-render

**Location**:

**Desktop** Settings → General → Other → Use texture render

Use texture rendering to make the pictures smoother. You could try disabling this option if you encounter rendering issues. Only available on desktop.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | linux:Y, macOS:N, win7:N, win10+:Y | `use-texture-render=Y` |

### enable-udp-punch

**Location**:

**Desktop** Settings → General → Other → Enable UDP hole punching
**Mobile** Settings → Enable UDP hole punching

Available since RustDesk 1.4.1, RustDesk Server Pro 1.6.2

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | Y | `enable-udp-punch=N` |

### enable-ipv6-punch

**Location**:

**Desktop** Settings → General → Other → Enable IPv6 P2P connection
**Mobile** Settings → General → Other → Enable IPv6 P2P connection

Available since RustDesk 1.4.1, RustDesk Server Pro 1.6.2

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | selfhost:N, otherwise:Y | `enable-ipv6-punch=N` |

## Display Settings

### view-only

This option will set the "view-only" option for every peer after the first connection.

Then the "view-only" option in each peer's settings will controls whether the connection is view-only.

**Location**:

1. **Desktop** Settings → Display → Other default options → View mode
2. **Mobile** Settings → Display settings → Other default options → View mode

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `view-only=Y` |

### show-monitors-toolbar

Controls whether to show monitors in toolbar.

![show-monitors-toolbar](/docs/en/self-host/client-configuration/advanced-settings/images/show-monitors-toolbar.png)

**Location**:

1. **Desktop** Settings → Display → Other default options → Show monitors toolbar
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `show-monitors-toolbar=Y` |

### collapse-toolbar

Controls whether the remote toolbar is collapsed after connecting.

**Location**:

1. **Desktop** Settings → Display → Other default options → Collapse toolbar
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `collapse-toolbar=Y` |

### show-remote-cursor

This option will set the "show-remote-cursor" option for every peer after the first connection.

Then the "show-remote-cursor" option in each peer's settings will controls whether the remote cursor is displayed in the remote control page.

**Location**:

1. **Desktop** Settings → Display → Other default options → Show remote cursor
2. **Mobile** Settings → Display settings → Other default options → Show remote cursor

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `show-remote-cursor=N` |

### follow-remote-cursor

This option will set the "follow-remote-cursor" option for every peer after the first connection.

Then the "follow-remote-cursor" option in each peer's settings will controls whether to follow the remote cursor.

**Preview**: [PR 7717](https://github.com/rustdesk/rustdesk/pull/7717)

**Location**:

1. **Desktop** Settings → Display → Other default options → Follow remote cursor
2. **Mobile** Settings → Display settings → Other default options → Follow remote cursor

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `follow-remote-cursor=Y` |

### follow-remote-window

This option will set the "follow-remote-window" option for every peer after the first connection.

Then the "follow-remote-window" option in each peer's settings will controls whether to follow the remote window.

**Preview**: [PR 7717](https://github.com/rustdesk/rustdesk/pull/7717)

**Location**:

1. **Desktop** Settings → Display → Other default options → Follow remote window focus
2. **Mobile** Settings → Display settings → Other default options → Follow remote window focus

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `follow-remote-window=Y` |

### zoom-cursor

This option will set the "zoom-cursor" option for every peer after the first connection.

The "zoom-cursor" option in each peer's settings will then control whether the cursor is scaled based on the current image scale.

**Location**:

1. **Desktop** Settings → Display → Other default options → Zoom cursor
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `zoom-cursor=Y` |

### show-quality-monitor

This option will set the "show-quality-monitor" option for every peer after the first connection.

The "show-quality-monitor" option in each peer's settings will then control whether to show the quality monitor.

**Location**:

1. **Desktop** Settings → Display → Other default options → Show quality monitor
2. **Mobile** Settings → Display settings → Other default options → Show quality monitor

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `show-quality-monitor=Y` |

### disable-audio

This option will set the "disable-audio" option for every peer after the first connection.

The "disable-audio" option in each peer's settings will then control whether to play sound.

**Location**:

1. **Desktop** Settings → Display → Other default options → Mute
2. **Mobile** Settings → Display settings → Other default options → Mute

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `disable-audio=Y` |

### enable-file-copy-paste

This option will set the "enable-file-copy-paste" option for every peer after the first connection.

The "enable-file-copy-paste" option in each peer's settings will then control enable file copy and paste in connection.

**Location**:

1. **Desktop** Settings → Display → Other default options → Enable file copy and paste (Windows only)
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `enable-file-copy-paste=Y` |

### disable-clipboard

This option will set the "disable-clipboard" option for every peer after the first connection.

The "disable-clipboard" option in each peer's settings will then control whether to enable text copy and paste.

**Location**:

1. **Desktop** Settings → Display → Other default options → Disable clipboard
2. **Mobile** Settings → Display settings → Other default options → Disable clipboard

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `disable-clipboard=Y` |

### lock-after-session-end

This option will set the "lock-after-session-end" option for every peer after the first connection.

The "lock-after-session-end" option in each peer's settings will then control whether to lock the peer machine after the session ends.

**Location**:

1. **Desktop** Settings → Display → Other default options → Lock after session end
2. **Mobile** Settings → Display settings → Other default options → Lock after session end

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `lock-after-session-end=Y` |

### privacy-mode

This option will set the "privacy-mode" option for every peer after the first connection.

The "privacy-mode" option in each peer's settings will then control whether to use privacy mode after connecting.

**Location**:

1. **Desktop** Settings → Display → Other default options → Privacy mode
2. **Mobile** Settings → Display settings → Other default options → Privacy mode

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `privacy-mode=Y` |

### touch-mode

This option will set the "touch-mode" option for every peer after the first connection.

The "touch-mode" option in each peer's settings will then control whether to use touch mode or mouse mode.

**Location**:

1. **Desktop**
2. **Mobile** Settings → Display settings → Other default options → Touch mode

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `touch-mode=Y` |

### i444

This option will set the "i444" option for every peer after the first connection.

The "i444" option in each peer's settings will then control whether to use true color.

**Location**:

1. **Desktop** Settings → Display → Other default options → True color (4:4:4)
2. **Mobile** Settings → Display settings → Other default options → True color (4:4:4)

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `i444=Y` |

### reverse-mouse-wheel

This option will set the "reverse-mouse-wheel" option for every peer after the first connection.

The "reverse-mouse-wheel" option in each peer's settings will then control whether to reverse mouse wheel.

**Location**:

1. **Desktop** Settings → Display → Other default options → Reverse mouse wheel
2. **Mobile** Settings → Display settings → Other default options → Reverse mouse wheel

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `reverse-mouse-wheel=Y` |

### swap-left-right-mouse

This option will set the "swap-left-right-mouse" option for every peer after the first connection.

The "swap-left-right-mouse" option in each peer's settings will then control whether to swap left-right mouse button.

**Location**:

1. **Desktop** Settings → Display → Other default options → Swap left-right mouse button
2. **Mobile** Settings → Display settings → Other default options → Swap left-right mouse button

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `swap-left-right-mouse=Y` |

### displays-as-individual-windows

This option will set the "displays-as-individual-windows" option for every peer after the first connection.

The "displays-as-individual-windows" option in each peer's settings will then control whether to show displays as individual windows.

**Preview**: [PR 5945](https://github.com/rustdesk/rustdesk/pull/5945)

**Location**:

1. **Desktop** Settings → Display → Other default options → Show displays as individual windows
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `displays-as-individual-windows=Y` |

### use-all-my-displays-for-the-remote-session

This option will set the "use-all-my-displays-for-the-remote-session" option for every peer after the first connection.

The "use-all-my-displays-for-the-remote_session" option in each peer's settings will then control whether to use all my displays for the remote session.

**Preview**: [PR 6064](https://github.com/rustdesk/rustdesk/pull/6064)

**Location**:

1. **Desktop** Settings → Display → Other default options → Use all my displays for the remote session
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `use-all-my-displays-for-the-remote-session=Y` |

### view-style

This option will set the "view-style" option for every peer after the first connection.

The "view-style" option in each peer's settings will then control the view style.

**Location**:

1. **Desktop** Settings → Display → Default view style
2. **Mobile** Settings → Display settings → Default view style

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | original, adaptive | original | `view-style=original` |

### scroll-style

This option will set the "scroll-style" option for every peer after the first connection.

The "scroll-style" option in each peer's settings will then control the scroll style.

**Location**:

1. **Desktop** Settings → Display → Default scroll style
2. **Mobile**

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | scrollauto, scrollbar | scrollauto | `scroll-style=scrollauto` |

### image-quality

This option will set the "image-quality" option for every peer after the first connection.

The "image-quality" option in each peer's settings will then control the image quality.

**Location**:

1. **Desktop** Settings → Display → Default image quality
2. **Mobile** Settings → Display settings → Default image quality

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | best, balanced, low, custom | balanced | `image-quality=balanced` |

### custom-image-quality

This option will set the "custom-image-quality" option for every peer after the first connection.

The "custom-image-quality" option in each peer's settings will then control the image quality if "image-quality" is set to custom.

**Location**:

1. **Desktop** Settings → Display → Default image quality → Custom
2. **Mobile** Settings → Display settings → Default image quality → Custom

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | [10.0, 2000.0] | 50.0 | `custom-image-quality=50` |

### custom-fps

This option will set the "custom-fps" option for every peer after the first connection.

The "custom-fps" option in each peer's settings will then control the fps if "image-quality" is set to custom.

**Location**:

1. **Desktop** Settings → Display → Default image quality → Custom
2. **Mobile** Settings → Display settings → Default image quality → Custom

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | [5, 120] | 30 | `custom-fps=30` |

### codec-preference

This option will set the "codec-preference" option for every peer after the first connection.

The "codec-preference" option in each peer's settings will then control codec for images.

**Location**:

1. **Desktop** Settings → Display → Default codec
2. **Mobile** Settings → Display settings → Default codec

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | auto, vp8, vp9, av1, h264, h265 | auto | `codec-preference=auto` |

**Caution**: Options other than "vp8" and "vp9" may not work. This depends on what your machine supports.

### terminal-persistent

This option will set the "terminal-persistent" option for every peer after the first connection.

The "terminal-persistent" option in each peer's settings will then control whether to keep terminal sessions on disconnect.

**Location**:

1. **Desktop** Settings → Display → Other default options → Keep terminal sessions on disconnect
2. **Mobile** Settings → Display settings → Other default options → Keep terminal sessions on disconnect

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `terminal-persistent=Y` |

### trackpad-speed

This option will set the "trackpad-speed" option for every peer after the first connection.

The "trackpad-speed" option in each peer's settings will then control the fps if "trackpad-speed" is set to custom.

**Location**:

1. **Desktop** Settings → Display → Default trackpad speed
2. **Mobile** Settings → Display settings → Default trackpad speed

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | [10, 1000] | 100 | `trackpad-speed=100` |

## Others

### preset-address-book-name & preset-address-book-tag

Preset address book name and tag, https://github.com/rustdesk/rustdesk-server-pro/issues/257.
You can set preset-address-book-name only if you do not want to set tag.
Please use valid address book name and tag on your address book page of web console.

| Option | Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: | :------: |
| preset-address-book-name | N | | | `preset-address-book-name=<address book name>` |
| preset-address-book-tag | N | | | `preset-address-book-tag=<address book tag name>` |

### disable-group-panel

Disable group panel (next to address book panel, it is named to "Accessible devices" since 1.3.8) on RustDesk client, https://github.com/rustdesk/rustdesk-server-pro/issues/250.

| Option | Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: | :------: |
| disable-group-panel | N | Y, N | N | `disable-group-panel=Y` |

### pre-elevate-service

Automatic elevation on run for Windows portable, https://github.com/rustdesk/rustdesk-server-pro/issues/252.

| Option | Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: | :------: |
| pre-elevate-service | N | Y, N | N | `pre-elevate-service=Y` |

### disable-floating-window

When the Android service starts, it will display a floating window, which helps prevent the system from killing the RustDesk service.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `disable-floating-window=Y` |

### floating-window-size

When the Android service starts, it will display a floating window, which helps prevent the system from killing the RustDesk service. When the size is less than 120, the floating window will be difficult to be clicked. A very small size may not be able to keep the background service on some devices.

| Values | Default | Example |
| :------: | :------: | :------: |
| [32, 320] | 120 | `floating-window-size=120` |

### floating-window-untouchable

By default, clicking on the floating window will pop up a menu. After setting it to 'untouchable', clicking or swiping will pass through the floating window and be transmitted to the underlying window. After being set to 'untouchable', the position of the floating window cannot be changed, and the system may automatically set the floating window to be semi-transparent. However, this feature may not work in a small number of applications, such as the GitHub app.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `floating-window-untouchable=Y` |

### floating-window-transparency

Android floating windows have adjustable transparency. If you want to enable but hide the floating window, you can set the transparency to 0, the floating window will be automatically set to 'untouchable' in order to pass through click events.

| Values | Default | Example |
| :------: | :------: | :------: |
| [0, 10] | 10 | `floating-window-transparency=5` |

### floating-window-svg

If an icon is not set for the Android floating window, it will default to displaying the RustDesk icon.
When setting, please write the text content of SVG into one line, and pay attention to the [SVG support limitations](https://bigbadaboom.github.io/androidsvg/index.html).

| Default | Example |
| :------: | :------: |
| RustDesk icon | `floating-window-svg=<?xml version="1.0" standalone="no"?><!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"><svg t="1717559129252" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4248" xmlns:xlink="http://www.w3.org/1999/xlink" width="32" height="32"><path d="M950.857143 512c0 242.285714-196.571429 438.857143-438.857143 438.857143S73.142857 754.285714 73.142857 512 269.714286 73.142857 512 73.142857s438.857143 196.571429 438.857143 438.857143z" fill="#1296db" p-id="4249"></path></svg>` |

### keep-screen-on

This is for the Android controlled side. Note that keeping the screen on depends on the floating window.

| Values | Default | Example |
| :------: | :------: | :------: |
| never, during-controlled, service-on | during-controlled | `keep-screen-on=never` |

### enable-directx-capture

This is for the Windows controlled side. If you don't encounter any problems, it is recommended to use the default settings, which prioritize using DirectX for screenshots instead of using GDI directly.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | Y | `enable-directx-capture=N` |

### enable-android-software-encoding-half-scale

This is for the Android controlled side. By default, when the resolution is greater than 1200, hardware encoding uses the original resolution, while software encoding uses half the resolution, as software encoding is slower. This option is used to set whether software encoding should be scaled to half the resolution.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | Y | `enable-android-software-encoding-half-scale=N` |

### allow-remote-cm-modification

Controls whether to allow the control side to click on the connection management window to accept connections, change permissions, etc.

https://github.com/rustdesk/rustdesk/issues/7425

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-remote-cm-modification=Y` |

### remove-preset-password-warning

Controls whether to remove the security warning on GUI when there is preset password in custom client. 

https://github.com/rustdesk/rustdesk-server-pro/discussions/286

https://github.com/rustdesk/rustdesk/discussions/7956

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | Y | `remove-preset-password-warning=Y` |

### hide-security-settings / hide-network-settings / hide-server-settings / hide-proxy-settings / hide-websocket-settings / hide-remote-printer-settings

Controls whether to hide some settings. Please ensure `Disable settings` is turned off, otherwise these won't work.

https://github.com/rustdesk/rustdesk-server-pro/issues/263

https://github.com/rustdesk/rustdesk-server-pro/issues/276

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `hide-security-settings=Y` |

### hide-username-on-card

Controls whether to show username in the list of devices. Because sometimes, the username is too long, will hide the other info.

https://github.com/rustdesk/rustdesk-server-pro/issues/284#issuecomment-2216521407

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `hide-username-on-card=Y` |

### hide-help-cards

Controls whether to show UAC / permission warnings on GUI.

https://github.com/rustdesk/rustdesk/issues/8687

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `hide-help-cards=Y` |

### display-name

Change your display name which will be shown on the popup when you connect to remote device. By default it displays login user's name first, otherwise it displays your OS username.

https://github.com/rustdesk/rustdesk-server-pro/issues/277

### disable-udp

Controls whether to use TCP only. It will not use UDP 21116 any more, TCP 21116 will be used instead.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `disable-udp=Y` |

### preset-user-name / preset-strategy-name / preset-device-group-name

Assign user / strategy / device group to device. You can also do this via [command line](https://rustdesk.com/docs/en/self-host/rustdesk-server-pro/console/#assign-device-usersgroupsstrategies-to-devices).

https://github.com/rustdesk/rustdesk-server-pro/discussions/304

device group is available in RustDesk client >=1.3.8, pro >= 1.5.0

### default-connect-password

You use the `default connection password` to establish connections to remote devices. This password is configured on the controlling side and should not be confused with any [preset password](https://github.com/rustdesk/rustdesk/wiki/FAQ#how-can-we-set-up-a-client-with-a-fixed-password-for-unattended-remote-access) found on the controlled (incoming-only) client.

e.g. `default-connect-password=abcd1234`

### enable-trusted-devices

Allow trusted devices to skip 2FA verification.

https://github.com/rustdesk/rustdesk/discussions/8513#discussioncomment-10234494

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | Y | `enable-trusted-devices=N` |

### hide-tray

Disable the tray icon in the systray.

https://github.com/rustdesk/rustdesk-server-pro/issues/332

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `hide-tray=Y` |

### one-way-clipboard-redirection

Disable clipboard sync from controlled side to controlling side, available in RustDesk client >=1.3.1 (controlled side)

https://github.com/rustdesk/rustdesk/discussions/7837

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `one-way-clipboard-redirection=Y` |

### one-way-file-transfer

Disable file transfer from controlled side to controlling side, available in RustDesk client >=1.3.1 (controlled side)

https://github.com/rustdesk/rustdesk/discussions/7837

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `one-way-file-transfer=Y` |


### sync-init-clipboard

If sync initial clipboard when establishing connection (only from controlling side to controlled side), available in RustDesk client >=1.3.1 (controlling side)

https://github.com/rustdesk/rustdesk/discussions/9010

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `sync-init-clipboard=Y` |

### allow-logon-screen-password

If allow password input on logon screen when [click-only approve mode](https://rustdesk.com/docs/en/self-host/client-configuration/advanced-settings/#approve-mode) is used, available in RustDesk client >=1.3.1 (controlled side)

https://github.com/rustdesk/rustdesk/discussions/9269

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-logon-screen-password=Y` |

### allow-https-21114

Typically, HTTPS uses port 443. When the API server's port is mistakenly set to 21114, RustDesk client will remove the 21114 port setting by default. Setting the option to Y allows the use of 21114 as the HTTPS port. Available in RustDesk client >=1.3.9.

https://github.com/rustdesk/rustdesk-server-pro/discussions/570

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-https-21114=Y` |

### allow-d3d-render

D3D render can get high FPS and reduce the cpu usage, but the remote control screen may be black on some devices. Available in RustDesk client >=1.3.9, windows only.

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-d3d-render=Y` |

### allow-hostname-as-id

[Use hostname as id](https://github.com/rustdesk/rustdesk-server-pro/discussions/483), spaces in the hostname are replaced with '-'. This is not 100% guaranteed and only occurs the first time the RustDesk client is run (i.e., on a newly installed client); if a conflict occurs, a random ID will be assigned. 

Available in RustDesk client version 1.4.0 and later. 

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-hostname-as-id=Y` |

### allow-websocket

Use WebSocket protocol to connect server and client. Only available in RustDesk client >=1.4.0 and Pro server >= 1.5.7. Note that WebSocket only supports relay connection.

To make WebSocket work, you need to configure your reverse proxy correctly, https://rustdesk.com/docs/en/self-host/rustdesk-server-pro/faq/#8-add-websocket-secure-wss-support-for-the-id-server-and-relay-server-to-enable-secure-communication-for-all-platforms

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-websocket=Y` |

### allow-numeric-one-time-password

This option enables or disables the use of numeric-only one-time passwords.
Only available in RustDesk client >=1.4.1 and Pro server >= 1.5.9.

**Discussion**: https://github.com/rustdesk/rustdesk-server-pro/discussions/685

**Preview**: https://github.com/rustdesk/rustdesk/pull/11846

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | N | `allow-numeric-one-time-password=Y` |

### register-device

Do not register the device, you will not see it in the devices page on web console. 

**Only available in Pro server >= 1.6.0 and requires [custom2 license](https://rustdesk.com/pricing#custom2) and number of concurrent connections >= 2.**

If `register-device=N`, below will not work for this device.
- Log in
- `--assign` command
- `preset-address-book-name`, `--preset-address-book-tag`, `preset-user-name`, `preset-strategy-name`, `preset-device-group-name`
- Audit Logs
- Strategy

**Discussion**: https://github.com/rustdesk/rustdesk-server-pro/discussions/672 and https://github.com/rustdesk/rustdesk-server-pro/discussions/182

| Values | Default | Example |
| :------: | :------: | :------: |
| Y, N | Y | `register-device=N` |

### main-window-always-on-top

Always keep the main window on top.

**Discussion**: https://github.com/rustdesk/rustdesk-server-pro/issues/761

Only available in RustDesk client 1.4.2.

| Install required | Values | Default | Example |
| :------: | :------: | :------: | :------: |
| N | Y, N | N | `main-window-always-on-top=N` |
