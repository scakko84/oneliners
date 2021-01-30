# oneliners
A collection of terminal oneliners

## Terminal

Replace spaces with dots in filenames recursively
```console
find . -depth -name "* *" -execdir rename 's/ /./g' "{}" \;
```

Copies directory to remote path via scp
```console
scp -r directory user@host:"'path/with spaces/'"
```

Delete all files matching multiple extensions recursively in directory
```console
find . \( -name '*.ext1' -or -name '*.ext2' \) -delete
```
Write image file to usb device
```console
dd if=file.img of=/dev/sdx bs=4M oflag=sync
```

## cURL

Download from URL to file resuming from last interruption
```console
curl -L -O -C - url -o file
```

## Wget

Download recursively from an URL all files of a given type to current directory
```console
wget -r -np -nd -nc -A "*.xyz" 'url'
```

## OpenSSL

Generate a pseudo-random password from secure random data
```console
openssl rand -base64 32
```

Download a server certificate in DER format from an endpoint
```console
openssl s_client -showcerts -servername www.example.com -connect www.example.com:443 < /dev/null | openssl x509 -outform DER > www.example.com.der
```

## MacOS

Convert iso file to img file
```console
hdiutil convert -format UDRW target.iso -o target.img
```
