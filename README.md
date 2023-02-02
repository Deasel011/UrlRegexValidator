# UrlRegexValidator
A C# style regex that can validate most URLs

```
^(?<protocol>https?://)?((?<ipaddress>([12]?(?(?<=2)[0-5]|(?(?<=1)[0-9]|[1-9]))?(?(?<=25)[0-5]|(?(?<=[0-9])[0-9]|[1-9]))\.){3}[12]?(?(?<=2)[0-5]|(?(?<=1)[0-9]|[1-9]))?(?(?<=25)[0-5]|(?(?<=[0-9])[0-9]|[1-9])))|(?<domain>[-a-zA-Z0-9@:%._\+~#=]{2,256})\.(?<topleveldomain>[a-zA-Z]{2,6}))(?<port>:[1-6]?(?(?<=[^6])\d{0,4}|[0-5](?(?<=[^5])\d{0,3}|[0-5](?(?<=[^5])\d{0,2}|[0-3](?(?<=[^3])\d?|[0-5]?)))))?(?<trailingpath>/[-a-zA-Z0-9@:%_\+.~#?&//=]*)?$
```
