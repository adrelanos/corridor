# Tor traffic whitelisting gateway #

There are several transparently torifying gateways. They suffer from the same
problems:

- It's tricky to isolate circuits and issue NEWNYM signals, especially if
multiple client computers are involved.
- Any garbage software can pump identifiers into "anonymous" circuits, and
get itself exploited by malicious exit nodes.
- Trust is centralized to the gateway, which is bad enough when used by one
person, and just inappropriate when shared with strangers.

corridor takes a different approach. It allows only connections to Tor relays
to pass through (no clearnet leaks!), but client computers are themselves
responsible for torifying their own traffic. In other words, it is a filtering
gateway, not a proxying gateway.

You can think of it as defense in depth for your vanilla Tor Browser or Tails,
for your beautiful scary experimental Qubes proxying schemes, etc. Or invite
the hood to use your WiFi without getting into trouble.
## How to install `corridor` using apt-get ##

1\. Add [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg adv --keyserver hkp://ipv4.pool.sks-keyservers.net:80 --recv-keys 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org stretch main" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `corridor`.

```
sudo apt-get install corridor
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `corridor` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Payments ##

`corridor` requires [payments](https://www.whonix.org/wiki/Payments) to stay alive!
