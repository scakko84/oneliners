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
find . \( -name '*.zip' -or -name '*.txt' \) -delete
```
Write image file to usb device
```console
dd if=file.img of=/dev/sdx bs=4M oflag=sync
```

## cURL

Download from URL to file resuming from last interruption
```console
curl -L -O -C - 'http://www.example.com/example.zip' -o example.zip
```

## Wget

Download recursively from an URL all files of a given type to current directory
```console
wget -r -np -nd -nc -A "*.zip" 'http://www.example.com/'
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

## macOS

Convert iso file to img file
```console
hdiutil convert -format UDRW target.iso -o target.img
```
