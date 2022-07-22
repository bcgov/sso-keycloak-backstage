The CSS App Redirect URI Format contains two parts
1. schema such as http, https, or customized image-cc. It contains * may contains '-' or '.'
2. path which starts with ://
 * at least 1 non whitespace alphanumeric character
 * must be atleast one character long

This is the regular expression (/^[a-zA-Z][a-zA-Z-\.]*:\/\/\S+/))