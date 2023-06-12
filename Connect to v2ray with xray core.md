At first install xray-core, i suggest you to install beta version, because just beta version has supported `Reality` method. But if you wont to use reality method and you have other config configuration use latest version.

```bash
bash -c "$(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh)" @ install --beta
```

Then put your json config into `/usr/local/etc/xray/config.json` file.
```bash
vim /usr/local/etc/xray/config.json
```

Then restart xray service:
```bash
systemctl restart xray
```

## Connect to proxy
For connect to your proxy you can set variable enviroments:
```bash
export HTTP_PROXY=http://localhost:10809
export HTTPS_PROXY=http://localhost:10809
export http_proxy=http://localhost:10809
export https_proxy=http://localhost:10809
```