# squid
https://squidanalyzer.darold.net/
* proxy setting
<pre>
    environment:
      LANG: en_US
      LANGUAGE: en_US
      LC_ALL: C
      LOCALE: en_US
      TZ: Asia/Shanghai
      LOGIN: admin
      PASS: Passw0rd
      PATHLOGS: /var/log/squid/access.log 
      http_proxy: http://squid:3128
      https_proxy: http://squid:3128
</pre>
* add corn
<pre>
docker-compose exec squidanalyzer /bin/bash -c "/usr/local/bin/squid-analyzer > /dev/null"
</pre>
* http://xxxxx:8090

