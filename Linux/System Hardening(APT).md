**Keeping the system up to date**
```
apt-get update
```
```
apt-get upgrade
```
<br>

**Ensuring only root has UID of 0**
```
awk -F: '($3=="0"){print}' /etc/passwd
```
<br>


**Checking accounts for empty passwords**
```
cat /etc/shadow | awk -F: '($2==""){print $1}'
```
<br>

**Locking accounts**
```
passwd -l accountName
```
