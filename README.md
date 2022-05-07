# PINS PARA LARAVEL
## Comandos desde ssh para Respaldo y Otros
### Respaldo de Mysql completo
   1. Generar el archivo de Contraseñas para Mysql.
      - `vi ~/.my.cnf`
      ```
      user=root_or_user
      password=********
      ```
   2. Crear el Comando de Respaldo.
```
root@server:~# vi resp.sh
d=´date +%Y_%m_%d_%H_%M´
mysqldump -u qubits_root <cliente> > /home/<cliente>/<cliente>_prd_$d.sql

cd /home/<cliente>
zip /home/<cliente>/<cliente>_prd_$d.zip /home/<cliente>/<cliente>_prd_$d.sql
rm /home/<cliente>/<cliente>_prd_$d.sql
echo "ejecutar en Git Bash"
echo "scp <cliente>@ip.ip.ip.52:/home/<cliente>/<cliente>_prd_$d.zip /c/lm/blackmind/proy/<cliente>/resp/<cliente>_prd_$d.zip"
```
   3. Ejecutar Comando de Respaldo
        - se ejecuta con . resp.sh
        - Luego, En Windows, con Git Bash:
            `scp <cliente>@ip.ip.ip.52:/home/<cliente>/<cliente>_prd_$d.zip /c/directorio/<cliente>/resp/<cliente>_prd_$d.zip`
