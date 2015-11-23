## Sample desktop files for GNOME desktop

Examples are based on [Free Desktop standards](http://standards.freedesktop.org/desktop-entry-spec/latest/) and demonstrate the most common uses of desktop files, but not all.

### Paths
User-space .desktop files can override the system wide in the typical way.

```
/home/alex/.local/share/applications/foo.desktop
```

Will **override**

```
/usr/share/applications/foo.desktop
```

Therefore we can add additional actions on apps.

```
/home/alex/.local/share/applications/firefox.desktop
```
Add some quick links on Firefox

```
...
Actions=open-google-youtube;open-gmail;

[Desktop Action open-youtube]
Name=YouTube
Exec=firefox https://www.youtube.com/

[Desktop Action open-gmail]
Name=YouTube
Exec=firefox https://www.gmail.com/
...

```

### Best practices

For quickly creating custom application files, create a desktop template on Gnome templates directory

```
$HOME/Templates/newDesktop.desktop
```

Then on
```
$HOME/.local/share/applications/
```

Right click in Gnome Files, `New Document-> newDesktop` and modify it!
