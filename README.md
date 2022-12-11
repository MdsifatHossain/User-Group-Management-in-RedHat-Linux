# User-Group-Management-in-RedHat-Linux

To show present uses terminal:
```
    #tty
```
*Linux have total six terminal

- (Alt + Ctrl + F1) --GUI(graphical terminal)
- (Alt + Ctrl +F2-F6) --command terminal

To show present uses all user terminal:
```
    #W
```
## User Management

Linux have three types of users:

- Root user 	id - 0
- System user	id  - 1 to 999
- Normal user/regular user	id -  1000+

1. To create user
```
    #adduser
```
2. Set user password:
```
    #passwd user name
```
3. To show user ID:
```
    $id user name 
```
4. To show user database:
```
    #cat /etc/passwd
    #cat /etc/passwd |less
```
5. To show user password related data:
```
    #cat /etc/shadow
```
6. To show last 10 line:
```
    #tail /etc/passwd
```
7. To show last n line:
```
    #tail -n /etc/passwd
```
8. To show specific user database:
```
    #cat /etc/passwd |grep username
    #tail /etc/shadow |grep user name
    #grep UID /etc/passwd
```
9. To show user account,password expiry date,warning date etc information:
```
    #chage -l username
```
10. To show user details:
```
    #lslogins user name
```
11. To set user password expire date:
```
    #chage -E YY-MM-DD user name
    #chage -E (number of days) user name
```
12. To set user password minimum days:
```
    #chage -m (number of days) user name
    #chage -m 10 sifat
```
13. To set user password maximum days:
```
    #chage -M (number of days) user name
    #chage -M 200 sifat
```
14. To set user password warning  days:
```
    #chage -W (number of days) user name
    #chage -W 7 sifat
```
15. All change in one command:
```
    #useradd -u UID -g primary group -G supplementary group -c "command" -d directory -s bash path -p password  user name
```
### Usermod command use to change all user information

1. To change user login name:
```
    #usermod -l new name old name
```
2. To add single existing user to the group:
```
    #usermod -aG group name user name
```
3. To add multiple group an existing user:
```
    #usermod -aG/Ga/G (multiple group name separated by comma) user name
    #usermod -aG group1,group2,group3... user name
```
4. To comment or comment modify:
```
    #usermod -c "comment" user name
```
5. To change user directory:
```
    #usermod -d directory path user name
```
6. To set or change user expire date:
```
    #usermod -e YY-MM-DD user name
```
7. To modify user ID :
```
    #usermod -u UID username
```
8. To give same UID existing multiple user:
```
    #usermod -o user name -u UID
```
9. To give same UID on new user:
```
    #useradd -o user name -u UID
```
10. To change user primary group:
```
    #usermod -g group name user name
```
11. To change user supplementary group:
```
    #usermod -G group name user name
```
12. To modify or change user password:
```
    #usermod -p password user name
```
13. To modify or change user login shell :
```
    #usermod -s shell path user name
```
14. To show present shell:
```
    #echo $SHELL
```
15. To show available shell:
```
    #cat /etc/shells
```
16. To create user without home directory:
```
    #useradd -M username
```
17. To create normal password to encrypted password:
```
    #openssl | passwd -crypt password 
```

## Group Management

*Linux have two types of Group :
- primary group
- Supplementary or secondary group 

1. To create a group :
```
    #groupadd group name
```
2. To show group ID:
```
    $id group name
```
3. To show group database:
```
    #cat /etc/group
    #tail /etc/group
```
4. To show specific group database:
```
    #cat /etc/group |grep group name 
    #tail /etc/group |grep 
    #grep group name /etc/group
```
5. To show group password related database:
```
    #cat /etc/gshadow
    #tail /etc/gshadow
```
6. To show specific database:
```
    #cat /etc/gshadow |grep group name 
    #tail /etc/gshadow |grep 
    #grep group name /etc/gshadow
```
7. Add multiple user to single group:
```
    #gpasswd -M user1,user2,user3... group name
```
8. Add single existing user to group:
```
    #usermod -G group name user name
    #gpasswd -a user name group name
```
9. New user add to supplementary group:
```
    #useradd -G group name user name
```
10. Add new user to multiple group:
```
    #useradd -G group1,group2,group3... user name
```
11. Add single user to multiple group:
```
    #usermod -G group1,group2,group3... user name
```
12. New user add to existing primary and secondary group:
```
    #useradd -g primary group name -G secondary single or multiple group name
    #useradd -g ict -G math,physics,chemistry
```
13. To change or modify group name:
```
    #groupmod -n new name old name
```
14. To change group ID:
```
    #groupmod -g ID group name
```
### Lock user, password and account:

1. To lock user password:
```
    #passwd -l user name
```
2. To unlock user password:
```
    #passwd -u username
```
3. To check lock status:
```
    #passwd -S user name
```
4. To lock user account:
```
    #usermod -L username
```
5. To unlock user account:
```
    #usermod -U user name
```
### Delete user and group

1. Delete user and group simple way:
```
    #userdel user name
    #groupdel group name
```
2. Delete user with home directory:
```
    #userdel -r user name
```
3. User delete with force:
```
    #userdel -f user name
```
4. Remove user from secondary group:
```
    #gpasswd -d user name group name
```


### Thank You

##### If you have any feedback, please reach out to me at mdsifathossain100@gmail.com
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/md-sifat-hossain-461274184/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/ict_all)

[@sifat](https://github.com/MdsifatHossain)

