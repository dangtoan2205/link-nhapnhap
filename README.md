```
scp ubuntu@192.168.90.12:/home/ubuntu/MailServer-Oxi-Offline-source.tar.gz .

tar -xzf .\MailServer-Oxi-Offline-source.tar.gz

cd .\MailServer-Oxi-Offline

docker build --platform linux/amd64 -t oxi-webmail:offline .
```
