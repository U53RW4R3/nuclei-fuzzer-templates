# nuclei-fuzzer-templates

I was trying to make it possible just like how the GET request method (you can grab it from [here](https://github.com/projectdiscovery/nuclei-templates/blob/main/http/vulnerabilities/generic/error-based-sql-injection.yaml)) passing the SQL payloads to inject the parameters. It's a waste that nobody made a POST request template-based.

`$ nuclei -u http://testphp.vulnweb.com/userinfo.php -t error-based-post-sql-injection.yaml -var username_forum=username_forums.txt -var password_forum=password_forums.txt -var path=sqli-payloads.txt`

## Credits

Special thanks to [fopwn](https://github.com/notnci) for providing me suggestions.
