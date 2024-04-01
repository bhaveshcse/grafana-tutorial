# grafana-tutorial
This is grafana tutorial repo.
1  mkdir grafana-config
    2  cd grafana-config/
    3  wget https://raw.githubusercontent.com/grafana/loki/v2.9.4/cmd/loki/loki-local-config.yaml -O loki-config.yaml
    4  docker run --name loki -d -v $(pwd):/mnt/config -p 3100:3100 grafana/loki:2.9.4 -config.file=/mnt/config/loki-config.yaml
    5  wget https://raw.githubusercontent.com/grafana/loki/v2.9.4/clients/cmd/promtail/promtail-docker-config.yaml -O promtail-config.yaml
    6  docker run --name promtail -d -v $(pwd):/mnt/config -v /var/log:/var/log --link loki grafana/promtail:2.9.4 -config.file=/mnt/config/promtail-config.yaml
    7  sudo apt  install docker.io
    8  sudo apt update
    9  sudo apt-get install -y docker.io
   10  wget https://raw.githubusercontent.com/grafana/loki/v2.9.4/cmd/loki/loki-local-config.yaml -O loki-config.yaml
   11  docker run --name loki -d -v $(pwd):/mnt/config -p 3100:3100 grafana/loki:2.9.4 -config.file=/mnt/config/loki-config.yaml
   12  wget https://raw.githubusercontent.com/grafana/loki/v2.9.4/clients/cmd/promtail/promtail-docker-config.yaml -O promtail-config.yaml
   13  docker run --name promtail -d -v $(pwd):/mnt/config -v /var/log:/var/log --link loki grafana/promtail:2.9.4 -config.file=/mnt/config/promtail-config.yaml
   14  ls -l
   15  sudo apt-get install -y apt-transport-https software-properties-common wget
   16  sudo mkdir -p /etc/apt/keyrings/
   17  wget -q -O - https://apt.grafana.com/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/grafana.gpg > /dev/null
   18  echo "deb [signed-by=/etc/apt/keyrings/grafana.gpg] https://apt.grafana.com stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
   19  echo "deb [signed-by=/etc/apt/keyrings/grafana.gpg] https://apt.grafana.com beta main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
   20  sudo apt-get update
   21  sudo apt-get install grafana
   22  sudo /bin/systemctl start grafana-server
   23  service grafana-server status
   24  history
