version: '3'

services:
  cisco-router:
    image: cisco/csr1000v
    ports:
      - "2222:22"  # Перенаправление порта SSH
    volumes:
      - ./configs:/configs  # Монтирование каталога с конфигурационными файлами
    command: ["sh", "-c", "cp /configs/* /etc/ssh/ && /usr/sbin/sshd -D"]
