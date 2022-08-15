# squid
https://squidanalyzer.darold.net/
* proxy setting for docker service
<pre>
    environment:
      http_proxy: http://squid:3128
      https_proxy: http://squid:3128
</pre>
* add cron
  sudo crontab -e
  <pre>
  * * * * * curl https://www.xyz.com/oauth2/ip > /dev/null
  </pre>
  sudo crontab -l
<pre>
docker-compose exec squidanalyzer /bin/bash -c "/usr/local/bin/squid-analyzer > /dev/null"
</pre>
* http://xxxxx:8090
<img src="./analyzer.png" />

