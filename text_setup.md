1: Thu vien goc cua odoo 
B1: 
volumes:
      # - ./odoo:/usr/lib/python3/dist-packages/odoo/addons/
      - ./config/odoo.conf:/etc/odoo/odoo.conf
      - ./addons:/mnt/extra-addons
      - ./log:/var/log/odoo
      - ./data:/var/lib/odoo
B2:
docker compose down
docker compose up -d
docker cp odoo18_web:/usr/lib/python3/dist-packages/odoo/addons/. ./odoo
B3:
volumes:
      - ./odoo:/usr/lib/python3/dist-packages/odoo/addons/
      - ./config/odoo.conf:/etc/odoo/odoo.conf
      - ./addons:/mnt/extra-addons
      - ./log:/var/log/odoo
      - ./data:/var/lib/odoo
odoo -> 
2: Thu vien DEV
addons -> 
3: Thu vien chua du lieu cac muc phat trien cua odoo
data ->
4: Thu vien chua database cua odoo
postgres_data ->
5: Chua thu vien goi du lieu cai dat odoo
requirements.txt 
6: Chua log cua odoo
log ->



----
Check Log Dokcer

docker logs odoo18_web --tail 100

--------
Mo quyen trong 

sudo chmod -R 777 .