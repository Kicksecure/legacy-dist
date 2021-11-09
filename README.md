# Prepare older Build Versions of Whonix for Upgrade #

Applies fixes required for upgrading from for example Whonix 8.x to Whonix
9.x etc.

Upgrades from Whonix 7.x or older versions is unsupported.

Safe to remove.
## How to install `whonix-legacy` using apt-get ##

1\. Download the APT Signing Key.

```
wget https://www.whonix.org/derivative.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add the APT Signing Key..

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.whonix.org bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `whonix-legacy`.

```
sudo apt-get install whonix-legacy
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `whonix-legacy`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`whonix-legacy` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
