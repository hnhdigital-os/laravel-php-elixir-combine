```
__________.__          ___________.__  .__       .__        
\______   \  |__ ______\_   _____/|  | |__|__  __|__|______ 
 |     ___/  |  \\____ \|    __)_ |  | |  \  \/  /  \_  __ \
 |    |   |   Y  \  |_> >        \|  |_|  |>    <|  ||  | \/
 |____|   |___|  /   __/_______  /|____/__/__/\_ \__||__|   
               \/|__|          \/               \/          
                                              Combine Module
```

Provides the ability to combine files together.

### Combine

Gets the contents of one or many files and combines it into the specified file.

Source folders can be specified with single level or multi-level lookup, and the ability to filter files by extension.

```
{DESTINATION_FILE}:
    - {SOURCE_FILE}
    - {SOURCE_FOLDER}
```

```yaml
combine:
    PATH_PUBLIC_ASSETS + /vendor/jquery-combined.min.js:
        - PATH_PUBLIC_ASSETS + /vendor/jquery/jquery.min.js
        - PATH_PUBLIC_ASSETS + /vendor/jquery-ui/jquery-ui.min.js
    PATH_PUBLIC_ASSETS + /vendor/combined.js:
        - PATH_PUBLIC_ASSETS + /vendor/**?filter=js

```