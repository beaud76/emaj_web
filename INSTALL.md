Emaj_web Installation Guide
===========================

1- Clone the github repository or Download ZIP
----------------------------------------------

Go to the https://github.com/dalibo/emaj_web URL and click on the "Clone or Download" button.

If you download the ZIP file, extract the zip package.

2- Configure Emaj_web
---------------------

Edit the conf/config.inc.php. 

It mainly deals with the configuration of PostgreSQL servers connections.

If you mess up the configuration file, you can recover it from the config.inc.php-dist file.

3- Browse to the Emaj_web installation using a web browser
----------------------------------------------------------

If the E-Maj extension is not installed on the database you connect on, or if the connection role is not granted emaj_adm or emaj_viewer rights, the E-Maj icon in the trail and in the left tree is not visible.

4- IMPORTANT - SECURITY
-----------------------

PostgreSQL by default does not require you to use a password to log in. We STRONGLY recommend that you enable md5 passwords for local connections in your pg_hba.conf, and set a password for the default superuser account.

In order to prevent risky connections, there is a configuration file option called 'extra_login_security', which is TRUE by default. While this option is enabled, you will be unable to log in to Emaj_web as the 'root', 'administrator', 'pgsql' or 'postgres' users and empty passwords will not work.
   
Once you are certain you have properly secured your database server, you can then disable 'extra_login_security' so that you can log in as your database administrator using the administrator password.
