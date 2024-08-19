To open a link on a device (i.e. a deep link):
```yaml
- openLink: https://example.com
```
If your app shows a disambiguation dialog along with other apps that can open the web link:
You can auto-verify the web link to be opened by your app with autoVerify attribute:
```yaml
- openLink: 
    link: https://example.com
    autoVerify: true
```
Beyond Android version 12, web links are by default opened in the web browser. It is possible for maestro to also auto-accept agreements of Google chrome if shown with the same autoVerify flag.
It is possible with maestro to force open web links with the web browser:
```yaml
- openLink: 
    link: https://example.com
    browser: true
```