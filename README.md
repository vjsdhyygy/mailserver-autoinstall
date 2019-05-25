邮件服务器  -  安装指南
==========================================

本一键包由法国 Antexa （https://github.com/Antexa/mailserver-autoinstall ） 编写  
讨论组 http://mondedie.fr/viewtopic.php?pid=11746 （打不开）
本人只是修改。

### 所需环境 :

- ``Debian 7 “wheezy”``
- ``Nginx`` // 准备删除该环境
- ``PHP``  //准备删除该环境
- ``MySQL`` //必须
- ``OpenSSL`` //必须

### 安装

```bash
apt-get update && apt-get dist-upgrade
apt-get install git-core
```

```bash
cd /tmp
git clone https://github.com/vjsdhyygy/mailserver-autoinstall.git
cd mailserver-autoinstall
chmod +x install.sh && ./install.sh
```

### 说明

Le script de désinstallation permet de supprimer absolument **TOUT** ce qu'à fait le script d'installation. Si vous avez une erreur pendant la configuration du serveur de mail, vous pouvez répartir à zéro avec ce script :
// 好吧，说明我看不懂， 貌似意思如果安装中有错误，可以用以下方式完全卸载（包含配置文件 / 暂时不建议使用
）
```bash
chmod +x uninstall.sh && ./uninstall.sh
```

Ce script est tiré du tutoriel "Installation sécurisée d'un serveur de mail avec Postfix, Dovecot et Rainloop" : http://mondedie.fr/viewtopic.php?id=5750

### Schéma

![schema](https://meshup.net/img/mail-server-tutorial/schema.png "schema")

Inspiré du script d'installation de rutorrent de ``Ex_Rat`` : https://bitbucket.org/exrat/install-rutorrent

### Support

Si vous avez une question, une remarque ou une suggestion, n'hésitez pas à poster un commentaire sur ce topic : http://mondedie.fr/viewtopic.php?id=5794

### License
MIT. Voir le fichier ``LICENCE`` pour plus de détails
