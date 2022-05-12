# Swarm DEB and RPM repos hosted on Github

## To add repo

### On Debian/Ubuntu

```
curl -fsSL https://repos.ethswarm.org/public.key | sudo gpg --dearmor -o /usr/share/keyrings/ethswarm-archive-keyring.gpg
```

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ethswarm-archive-keyring.gpg] https://repos.ethswarm.org/deb \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/ethswarm.list > /dev/null
```

### On CentOS/Fedora

```
echo "[ethersphere]
name=Ethersphere Repo
baseurl=https://repos.ethswarm.org/rpm
enabled=1
gpgcheck=1
gpgkey=https://repos.ethswarm.org/pgp-key.public" > /etc/yum.repos.d/ethersphere.repo
```
