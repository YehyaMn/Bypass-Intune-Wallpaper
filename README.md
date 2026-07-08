# Bypass-Intune-Wallpaper
```
$img="C:\Wallpapers\wallpaper.jpg"
$theme="$env:APPDATA\Microsoft\Windows\Themes"

Copy-Item $img "$theme\TranscodedWallpaper" -Force
Remove-Item "$theme\CachedFiles\*" -Force -ErrorAction SilentlyContinue

Stop-Process -Name explorer -Force
Start-Process explorer

Then put it schedule on logon
```
