<h1 align="center">SQL SERVER</h1>

# RESTAURAR DATABASE
 - copiar backup dentro del contenedor
 - ejecutar dentro del contenedor 
 - RESTORE FILELISTONLY FROM DISK = '/var/opt/mssql/backup/backup_matrix_mod.bak' 
 - Saldran estos datos
 - C:\Program Files\Microsoft SQL Server\MSSQL12.MSSQLSERVER\MSSQL\DATA\matrix_data.mdf
C:\Program Files\Microsoft SQL Server\MSSQL12.MSSQLSERVER\MSSQL\DATA\matrix_log.ldf 
 - seleccionas database master
 - RESTORE DATABASE matrix 
FROM DISK = '/var/opt/mssql/backup/backup_matrix_mod.bak'
WITH MOVE 'MATRIX' TO '/var/opt/mssql/data/matrix_data.mdf', 
MOVE 'MATRIX_log' TO '/var/opt/mssql/data/matrix_log.ldf'