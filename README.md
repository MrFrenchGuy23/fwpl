# FWPL v1.0 - First Release

**Please report any bugs to `defnotsrilankan23` on Discord.**

## Features

### Forwarding & Server Redirection

* **ServerConnectListener**

  * Sends players to the configured lobby/default server when they join.
  * Uses HIGH priority to override nAntiBot's default connection handling.

* **ServerKickListener**

  * Catches server kicks, crashes, and restarts.
  * Redirects players to another available server instead of disconnecting them.

* **AutoRedirectListener**

  * A 1-second fallback that checks for players left on the proxy without a server.
  * Automatically sends them to the configured lobby if needed.

* **Server Selection**

  * Case-insensitive server name matching.
  * Tries configured fallback servers first, then any registered server, and finally the server that issued the kick as a last resort.

### Friend System

* `/friend add`
* `/friend remove`
* `/friend accept`
* `/friend deny`
* `/friend list`

Includes tab completion for all friend commands.

* Sends notifications when friends join the network or switch servers.
* Uses MySQL for storage.
* Automatically disables database features if MySQL is unavailable to prevent console errors and NullPointerException spam.

### Configuration

* Configurable messages.
* Configurable MySQL connection settings in `config.yml`.

