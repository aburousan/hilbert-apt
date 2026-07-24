# Hilbert apt repository

An apt repository for [Hilbert](https://github.com/aburousan/hilbert-editor), an
offline desktop editor for Typst, for Debian and Ubuntu based systems (amd64).

## Install

```sh
curl -fsSL https://aburousan.github.io/hilbert-apt/hilbert-archive-keyring.asc \
  | sudo gpg --dearmor -o /usr/share/keyrings/hilbert-archive-keyring.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/hilbert-archive-keyring.gpg] https://aburousan.github.io/hilbert-apt stable main" \
  | sudo tee /etc/apt/sources.list.d/hilbert.list

sudo apt update
sudo apt install hilbert
```

## Update

```sh
sudo apt update && sudo apt upgrade hilbert
```

The signing key fingerprint is `F969 17DA CE94 1FE6 5A69  9994 7F9A AE54 09F2 976C`.
