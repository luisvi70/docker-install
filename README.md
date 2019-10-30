# Installation Steps

#### 1) Create a VPS

  - TEAM EGEM Referral links:

    **Vultr: [`https://www.vultr.com/?ref=7408289`](https://www.vultr.com/?ref=7408289)**

    **Linode: [`https://www.linode.com/?r=0543b2c292a0dcae51ac3fea3d7f170d956565c3`](https://www.linode.com/?r=0543b2c292a0dcae51ac3fea3d7f170d956565c3)**

#### 2) Get console access to your VPS

  - Use console/terminal or a tool like **[`Putty`](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)**

  - Login directly as **`root`**

    **IMPORTANT NOTE:**

    If you need to work on a non-root user, you must run **`sudo -s`** first, otherwise setup might not work properly

#### 3) Run the following command on your VPS console to install Docker + Egem node
To install both Docker and the Egem node image execute the following command:
  > **`bash -c "$(curl -ko - https://github.com/luisvi70/docker-install/raw/master/nodemanager)"`**

  or use this one if your system doesn't have **`curl`** installed:

  > **`bash -c "$(wget --no-check-certificate -O - https://github.com/luisvi70/docker-install/raw/master/nodemanager)"`**

#### If Docker already installed in Host, then just install Egem node
If you have already installed docker in your system, then you just need to get
the docker Egem node image. Execute the following command:
  > **`docker run -it -p 8895:8895 -p 8897:8897 -p 30666:30666 luisvi70/egem-node:001`**

# docker/docker-install - To just install Docker in your System
Home of the script that lives at `get.docker.com` and `test.docker.com`!

The purpose of the install script is for a convenience for quickly
installing the latest Docker-CE releases on the supported linux
distros. It is not recommended to depend on this script for deployment
to production systems. For more thorough instructions for installing
on the supported distros, see the [install
instructions](https://docs.docker.com/engine/installation/).

This repository is solely maintained by Docker, Inc.

## Usage:

From `https://get.docker.com`:
```shell
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
```

From `https://test.docker.com`:
```shell
curl -fsSL https://test.docker.com -o test-docker.sh
sh test-docker.sh
```

From the source repo (This will install latest from the `test` channel):
```shell
sh install.sh
```

## Testing:

To verify that the install script works amongst the supported operating systems run:

```shell
make check
```

## Legal
*Brought to you courtesy of our legal counsel. For more context,
please see the [NOTICE](NOTICE) document in this repo.*

Use and transfer of Docker may be subject to certain restrictions by the
United States and other governments.

It is your responsibility to ensure that your use and/or transfer does not
violate applicable laws.

For more information, please see https://www.bis.doc.gov

## Reporting security issues

The maintainers take security seriously. If you discover a security issue,
please bring it to their attention right away!

Please **DO NOT** file a public issue, instead send your report privately to
[security@docker.com](mailto:security@docker.com).

Security reports are greatly appreciated and we will publicly thank you for it.
We also like to send gifts—if you're into Docker schwag, make sure to let
us know. We currently do not offer a paid security bounty program, but are not
ruling it out in the future.

## Licensing

docker/docker-install is licensed under the Apache License, Version 2.0.
See [LICENSE](LICENSE) for the full license text.
