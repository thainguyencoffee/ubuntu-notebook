# ubuntu-install-tools


## Install docker
```bash
sudo apt update
```

```bashh
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

```bash
apt-cache policy docker-ce
```
Output of apt-cache policy docker-ce
```
docker-ce:
  Installed: (none)
  Candidate: 5:19.03.9~3-0~ubuntu-focal
  Version table:
     5:19.03.9~3-0~ubuntu-focal 500
        500 https://download.docker.com/linux/ubuntu focal/stable amd64 Packages
```

```bash
sudo apt install docker-ce
```

Check status for docker
```bash
sudo systemctl status docker
```

### Executing the Docker Command Without Sudo (Optional)

```bash
sudo usermod -aG docker ${USER}
```
To apply the new group membership, log out of the server and back in, or type the following:
```
su - ${USER}
```

## Docker compose
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```bash
sudo chmod +x /usr/local/bin/docker-compose
```

```bash
docker-compose --version
```

## Curl
```bash
sudo apt install curl -y
```

## Minikube (Kubernetes in local)
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```

```bash
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
```

## Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Grype
```bash
brew tap anchore/grype
```

```bash
brew install grype
```

## Tilt
```bash
brew install tilt-dev/tap/tilt
```

### Octant
Download: [Octant](https://github.com/vmware-archive/octant/releases/download/v0.25.1/octant_0.25.1_Linux-64bit.deb)

```bash
sudo dpkg -i ./Downloads/octant_0.25.1_Linux-64bit.deb
```

## Remove snap (Important)
```bash
sudo snap list
```

```bash
sudo apt purge snapd
```

## Install flatpak
```bash
sudo apt install flatpak -y
```
Add flatpak repository
```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

## Nala
```bash
sudo apt install nala
```

### Install pacstall
```bash
sudo bash -c "$(curl -fsSL https://pacstall.dev/q/install || wget -q https://pacstall.dev/q/install -O -)"
```

```bash
pacstall -I nala-deb
```
_pick 1  >> Ctrl + O >> Enter >> Ctrl + X_

```bash
sudo nala fetch
```
Typing `1 2 3` >> Enter

## Stacer
Download [Stacer](https://github.com/oguzhaninan/Stacer/releases/download/v1.1.0/stacer_1.1.0_amd64.deb)

```bash
sudo dpkg -i ./Downloads/stacer_1.1.0_amd64.deb
```

## Preload (running application faster)
```bash
sudo nala install preload
```
YES

### Tlp
```bash
sudo nala install tlp tlp-rdw
```
YES

```bash
sudo systemctl enable tlp
```

```bash
sudo systemctl start tlp
```

Checking
```bash
sudo systemctl status tlp
```

## End.
