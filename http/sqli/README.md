I was trying to make it possible just like how the GET request method (you can grab it from [here](https://github.com/projectdiscovery/nuclei-templates/blob/main/http/vulnerabilities/generic/error-based-sql-injection.yaml)) passing the SQL payloads to inject the parameters. It's a waste that nobody made a POST request template-based. Basically all this template does bruteforces the forums until it responds with the right set of parameters. Then passing the SQLi payloads is the final result.

`$ nuclei -u "http://testphp.vulnweb.com/userinfo.php" -t nuclei-fuzzer-templates -id error-based-post-sql-injection`

If you specifically want to perform a vulnerability assessment on GET request URLs then exclude the nuclei template ID.

`$ nuclei -u "http://testphp.vulnweb.com/artists.php?artist=1" -t nuclei-fuzzer-templates -tags sqli -eid error-based-post-sql-injection`
