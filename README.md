# squid
https://squidanalyzer.darold.net/
* proxy setting for docker service
<pre>
    environment:
      http_proxy: http://squid:3128
      https_proxy: http://squid:3128
</pre>
* add corn
<pre>
docker-compose exec squidanalyzer /bin/bash -c "/usr/local/bin/squid-analyzer > /dev/null"
</pre>
* http://xxxxx:8090
<img src="./analyzer.png" />

