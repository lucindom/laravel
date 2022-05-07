* PINS PARA LARAVEL
** Comandos desde ssh para Respaldo y Otros
*** Respaldo de Mysql completo
    - `root@server:~# vi resp.sh
d=`date +%Y_%m_%d_%H_%M`
mysqldump -u qubits_root <cliente> > /home/<cliente>/<cliente>_prd_$d.sql

cd /home/<cliente>
zip /home/<cliente>/<cliente>_prd_$d.zip /home/<cliente>/<cliente>_prd_$d.sql
rm /home/<cliente>/<cliente>_prd_$d.sql
echo "ejecutar en Git Bash"
echo "scp <cliente>@ip.ip.ip.52:/home/<cliente>/<cliente>_prd_$d.zip /c/lm/blackmind/proy/<cliente>/resp/<cliente>_prd_$d.zip"

se ejecuta con . resp.sh

Luego, En Windows, con Git Bash:
scp <cliente>@ip.ip.ip.52:/home/<cliente>/<cliente>_prd_$d.zip /c/lm/blackmind/proy/<cliente>/resp/<cliente>_prd_$d.zip`
