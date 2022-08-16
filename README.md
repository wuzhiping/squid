# squid
https://squidanalyzer.darold.net/
* proxy setting for docker service

# mkdir -p /etc/systemd/system/docker.service.d

<pre>
# cat > /etc/systemd/system/docker.service.d/http-proxy.conf << EOF

[Service]
Environment="HTTP_PROXY=http://your.proxy:8080"
Environment="HTTPS_PROXY=http://your.proxy:8080"
Environment="NO_PROXY=127.0.0.1,localhost
EOF

# systemctl daemon-reload
# systemctl restart docker
</pre>

<pre>
    environment:
      http_proxy: http://squid:3128
      https_proxy: http://squid:3128
      ftp_proxy: http://squid:3128
      rsync_proxy: http://squid:3128
      no_proxy: "localhost,127.0.0.1,localaddress,localdomain.com"
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

