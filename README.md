(1)$ ls /bin
(2)$ ls /tmp
(3)$ ls -dr /etc/t*
(4)$ ls /dev/tty??
(5)$ ls /dev/tty*[1-4]
(6)$ ls /dev/t*C1
(7)$ ls -a /
(8)$ ls -d /etc/[^
(9)$ ls -R /usr
(10)$ cd /tmp
(11)$ pwd
(12)$ date +"%A %D - %r" #ó simplemente DATE
(13)$ cd /HOME
(14)$ pwd
(15)$ ls -i
(16)mkdir PRUEBAtouch PRUEBA/{.f_hidden1,.f_hidden2,.f_hidden3}touch PRUEBA/{file1,file2,file3}mkdir PRUEBA/{dir1,dir2,dir3}$ rm -rf PRUEBA/*
(17)$ mkdir PRUEBA/{ dir1,\          dir1/dir11,\                  dir2,\                  dir3,\                    dir3/dir31,\                    dir3/dir31/dir311,\                    dir3/dir31/dir312}(18)$ cp /etc/motd ./PRUEBA
(18)$ cp /etc/motd ./PRUEBA
(19)$ cd PRUEBA$ cp mensaje dir1/mensaje && cp mensaje dir2/mensaje && cp mensaje dir3/mensaje
(20)$ ls -R PRUEBA
(21)$ cp -r /etc/rc.d dir
(22)$ cp -r /bin/?a?? PRUEBA/dir3/dir31/dir311(23)$ sudo cp -r ../user_other  PRUEBA/dir1/dir11$ cp -r ../user             PRUEBA/dir1/dir11
(24)$ mv PRUEBA/dir3/dir31 PRUEBA/dir2
(25)$ ls -R $HOME
(26)$ mv PRUEBA/dir3/mensaje PRUEBA/dir3/.mensaje
(27)$ rm -rf PRUEBA/dir1
(28)$ ls /dev/t???[a*b]
(29)$ find dir312 -type f -regex ".*???q[^b$]" -exec rm -r {} \;
(30)$ mv PRUEBA/dir2/dir31/dir312 PRUEBA/dir3(31)$ ln -s /home/usuario1/PRUEBA/dir1 PRUEBA/dir3/enlacedir1
(32)$ cd PRUEBA/dir3$ mkdir enlacedir1/nuevo1
(33)$ cp -r /bin/u* enlacedir1/nuevo1/
(34)$ ln fich1 dir1/enlace$ ln fich1 dir2/enlace
(35)$ rm fich1$ cp dir1/enlace dir3/$ ln -s /home/usuario1/PRUEBA/dir2/enlace /home/usuario1/PRUEBA/dir1/enlafich1(36)$ ln -s dir2/enlace dir1/enlafich1
36)$ ln -s dir2/enlace dir1/enlafich1
(37)$ cd dir1dir1$ cp enlafich1 ../dir2/dir31/dir311/fich1
(38)dir1$ cat enlafich1
(39)PRUEBA$ rm dir2/fich1
(40)$ rm -r *
(41)$ mkdir dir1 dir2
(42)$ chmod = dir1
(43)$ chmod 751 dir2
(44)$ ls -la ./dir2
(45)$ mkdir dir2/dir21  no se puede crear
(46)$ chmod 200 dir1$ ls -l$ mkdir dir1/dir21mkdir: no se puede crear el directorio «dir1/dir21»: Permiso denegado
(47)$ touch dir1/{file1,file2,file3}PRUEBA$ ls -l dir1
(48)$ ls  dir1  dir2  dir3$ mv dir1 dir3/$ ls -lR  .:  ./dir2:  ./dir2/dir21:  ./dir3:  ./dir3/dir1:
(49)./dir3
50)umask 0033
(51)$ mkdir dira dirb dirc dird
(52)$ ls -l
(53)$ touch uno$ chmod a-r uno$ ls -l$ rm uno$ _
(54)$ chmod = dir2$ chmod o=rwx dir2
(55)$ mkdir carpeta1 carpeta2$ chmod u=rwx,g=,o=   carpeta1$ chmod u=rwx,g=rx,o= carpeta2$ ls -l$ touch carpeta1/{fich1,fich2}  $ chmod = carpeta1/{fich1,fich2}  $ chmod o=rw         carpeta1/fich1  $ ls -l carpeta1$ touch carpeta2/{file1,file2}$ chmod = carpeta2/{file1,file2}$ chmod u=rw,g=rw carpeta2/file1$ chmod u=rw,g=r  carpeta2/file2  $ ls -l carpeta2
(56)$ su us3rlinux  Contraseña: ## carpeta1 ### prueba de accesous3rlinux@equipo1:/home/usuario1/PRUEBA$ cd carpeta1 bash: cd: carpeta1: Permiso denegado# prueba de lecturaus3rlinux@equipo1:/home/usuario1/PRUEBA$ ls carpeta1 ls: no se puede abrir el directorio carpeta1: Permiso denegado## carpeta2 ### prueba de accesous3rlinux@equipo1:/home/usuario1/PRUEBA$ cd carpeta2# prueba de lecturaus3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ ls -l
total  0
-rw-rw---- 1 usuario1 usuario1 0 2009-12-08 09:41 file1 -rw-r----- 1 usuario1 usuario1 0 2009-12-08 09:41 file2# prueba de lecturaus3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ cat file1us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ cat file2# prueba de escrituraus3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ echo 'hola' > file1us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ echo 'hola' > file2bash: file2: Permiso denegadoexitus3rlinux@equipo1:/home/usuario1/PRUEBA$ whoamius3rlinuxus3rlinux@equipo1:/home/usuario1/PRUEBA$ exitexitusuario1@equipo1:~/PRUEBA$ whoamiusuario1usuario1@equipo1:~/PRUEBA$
(57)$ pwd/home/usuario1/PRUEBA$ mkdir correo fuentes
(58)$ cd fuentes$ mkdir dir1 dir2(59)mkdir ../correo/menus
(60)$ cd $HOME$ find PRUEBA/fuentes -type d -name "*1" -exec rm -r {} \;
(61)$ find PRUEBA/fuentes/* -type d -regex ".*[0,2,3,4,5,6,7,8,9]" -exec rm -r {} \;$ find PRUEBA/fuentes/* -type d -regex ".*[^1]" -exec rm -r {} \;
(62)$ ls -l /dev/tt*
(63)$ find /usr/bin -type f
(64)$ ls /$ find / -maxdepth 1 -type d
(65)$ find / -user root -type 
(66)$ find /usr/include -type f -regex ".*.h"
(67)$ ls /bin/ls*
(68)$ find /home/us3rlinux -exec file --mime-type -0 '{}' \;
(69)$ mkdir uno$ chmod u=rw,g=rw,o= uno$ ls -ld uno
(70)$ chmod u=rwx,g=rwx,o= uno$ mkdir uno/uno1$ chmod u=rwx,g=,o=w uno/uno1$ ls -ld uno/uno1
(71)$ find /home/usuario1 -type f -regex ".*[0-9]" -exec cp -r '{}' PRUEBA/correo/menus/ \;
(72)$ sudo -s
(73)touch archivo_tamaño_cero
(74)$ cat /etc/motd0 packages can be updated.0 updates are security updates.
(75) $ who | grep $USER | sort -k 4 > persona
(76)$ mkdir carpeta$ chmod a-r carpeta$ find ~ -type d > direc
(77)$ find ~ -type d 2> malo
(78)$ find /etc -type f  >> direc
(79)$ find ./ -type f -not -iname *ai* 1> nuevalista 2> malos$ find ./ -type f -iname *ai* 1> nuevalista 2> malos(80
(80) time `sleep 3`$ time who -p %e
(81)$ ps -U root -u root u
(82)$ ps -U root -u root u | grep -v "`ls /dev`"
(83)$ echo "`date +"%A %D"` - `pwd`" >>nuevalista
(84)$ ps axu
(85)$ top -d .1 -n 10
(86)
(87)$ cat /etc/passwd | wc -l
(88)$ cat /etc/passwd | grep bash
(89)$ who -q
(90)$ man gcc > gcc.man_page$ cat gcc.man_page | sed -e 's/       //g' > file.filled$ cat file.filled | grep ^[Ll]
(91)$ cat file.filled | grep ^[Ll] | wc -l
(92)$ cat /etc/passwd | cut -d ':' -f 1
(93)$ gawk  -F: '{print $1, $7}' /etc/passwd
(94)$ touch -t 9910011101 good$ ls -l good
(95)$ md5sum good(96)$ md5sum good > good.MD5$ echo hola >> good
(96)$ md5sum good > good.MD5$ echo hola >> goo
$ md5sum -c good.MD5$ md5sum good
(97)$ df -lh
(98)for x in `seq 1 10`; do ps -eo pid,pcpu,pmem,user,args | sort -r -k 2 | head -n 2; sleep 3; done
(99)$ ps -eo pid,pcpu,pmem,user,args | grep bash$ ps a | grep bash
(100)$ ps -eo args | cut -d ' ' -f 1 | grep ^g | wc -
