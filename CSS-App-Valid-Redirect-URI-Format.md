In the CSS app, the allowed URI syntax consists of two parts with `://` in the middle:
- `<scheme>://<path>`
- `scheme`: the following rules must be met for the `scheme` part:
    1. must be greater than one character.
    2. must start with an alphabet character followed by optional characters (alphabets, hyphens(-), and periods(.))
- `path`: any characters are allowed except for white spaces.
- please refer to the regular expression `/^[a-zA-Z][a-zA-Z-\.]*:\/\/\S+/`