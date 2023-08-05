For running and debugging in Windows we need to auth in the installed Chrome using the `tmp/gphotos-cdp` as data dir to be pciked up by Chromium.

* In PowerShell run:
```
'C:\Program Files (x86)\Google\Chrome\Application\chrome.exe' `
    --no-first-run `
    --pasword-store=basic `
    --use-mock-keychain `
    --user-data-dir=C:\Users\Dany\AppData\Local\Temp\gphotos-cdp `
    https://photos.google.com
```
* Authenticate in the started Chrome windows.
* Close once done.
* Start program with `-dev` (to use `tmp/gphotos-cdp`)
```
go run .\main.go -v -dev -headless -dldir C:\Users\Dany\Downloads\gphotos
```