# UrlRegexValidator
A C# style regex that can validate most URLs

```
^(?<protocol>https?://)?((?<ipaddress>([12]?(?(?<=2)[0-5]|(?(?<=1)[0-9]|[1-9]))?(?(?<=25)[0-5]|(?(?<=[0-9])[0-9]|[1-9]))\.){3}[12]?(?(?<=2)[0-5]|(?(?<=1)[0-9]|[1-9]))?(?(?<=25)[0-5]|(?(?<=[0-9])[0-9]|[1-9])))|(?<domain>([-a-zA-Z0-9]{1,63}\.){0,3}[-a-zA-Z0-9]{1,63})\.(?<topleveldomain>[a-zA-Z]{2,6}))(?<port>:[1-6]?(?(?<=[^6])\d{0,4}|[0-5](?(?<=[^5])\d{0,3}|[0-5](?(?<=[^5])\d{0,2}|[0-3](?(?<=[^3])\d?|[0-5]?)))))?(?<trailingpath>/[-a-zA-Z0-9@:%_\+.~#?&//=]*)?$
```

## Does not match the following
```
1.2.3.256
10.6.2.67;8000
https://mydomain.com65535
http://specialcharacter@site.io:80
http://64charactersudlajflkjdlkgjldkgjldkfjkldjkldjgfdlkfjgldkfgldkfjhg.com/
http://portTooHigh.com:65536/
http://toosmalltopleveldomain.a/
```

## Matches the following
```
http://63charactersudlajflkjdlkgjldkgldkfjkldjkldjgfdlkfjgldkfgldkfjhg.com/
Pleasekeepinmindthatthisismostlytohelpwithtypos.Wearecomingfrom0validation-MORE-THAN-63.com
http://a.io:80
10.3.54.12
1.54.78.23
192.168.2.1
1.1.1.1
1.1.1.255
10.2.145.1:8000
10.2.145.1:65000
http://10.3.56.12
http://10.3.56.12/
http://10.3.56.12:8080
http://10.3.56.12:8080/
https://10.3.56.12
https://10.3.56.12/
https://10.3.56.12:8080
https://10.3.56.12:8080/
http://my.site.io:80
https://dev.some.company.cloud/a-nice-path/16788434674?nicest=true
mydomain.com
mydomain.com:8080
http://mydomain.com
http://mydomain.com/
http://mydomain.com:8080
http://mydomain.com:8080/
https://mydomain.com
https://mydomain.com/
https://mydomain.com:8080
https://mydomain.com:8080/
```

https://regex101.com/r/FFrhua/1
