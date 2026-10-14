This is a brute-force tool that uses IP rotation (specifically, the one provided by the Tor network); it is only compatible with Linux or Git Bash.

This will NEVER replace a paid automatic rotation service (there are many proxies that offer the same functionality as this code but are 30 times faster); this is just a free option that I programmed—please keep that in mind

Steps to use this tool

Run: docker pull netaru3/tornet
docker run -d --name tornetnetaru3/tornet:latest 
docker exec -it tornet5 /bin/bash

If you want to use tornet without Docker, download tor,haproxy and clone this repository

3: Once you’ve started Tor, just run the “tornet” command. Use the “- -url“ to specify the URL, ”-n“ to specify the number of requests to make before hitting the rate limit, ”--wordlist“ to specify the wordlist you want to use, ”--body“ to specify the response body (as a string), ”--error“ to specify the error message, and ”--header" to specify the response header.

What should the body look like?

The body must contain the “password” variable in the second position and be a JSON object cast as a string. For example, the command: tornet --body '{“username”:“realuser123”,‘password’:“PASSWD”}'

What should the header look like?

In the header, you only need to specify the type, for example: tornet --header “application/json”
