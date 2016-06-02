---
layout: post
title: django + Microsoft SQL Server
date:  2016-06-02 13:17:35
comments: true
published: false
categories: django pymssql mssql sql server microsoft python3.4 python3 python
---
## Backstory
Everybody has one of those bad days. When you get to work and try to ssh in to your server at home all of a sudden it says

    ssh: connect to host theimpaler.dlinkddns.com port 222: Connection timed out

You have no idea what's going on and you can't even call home because no one's there. So now you're just stuck at work doing your job, but that tiny piece of mind is busy thinking "what the hell happened to the server".

Finally, you get to your house and realize that when your 3 years old daughter was playing with a ball she accidentally hit the server, because you were dumb enough to leave the server in an open area. So your server is dead now. 

This is exactly what happened to me yesterday. Lucky me, my server still seems salvageable. However, because of my other more important projects I don't have time for restoring it right now. The only thing that I needed from it was my postgres database. Instead of restoring the machine just to get back my database, I decided to go with VirtualBox. Main reason for going this route is that I want to be sure that my Academic Management System is going to work with any database engine (not just postgres) and I chose Microsoft SQL Server. Thanks for the accident, Kumush!

## MSSQL Setup
I didn't want to have the whole professional environment working on my VirtualBox so I just went ahead with SQLEXPRESS version of MSSQL. The setup process was smooth and easy.

After the installation, I set up my database and users, and tested all the connections: everything is working in my local virtualbox environment.

### MSQQL TCP/IP Connection
SQLEXPRESS doesn't allow network connections by default. Therefore, now that our database is setup, we have to allow ourselves to connect to the mssql server over the network.

- Start *SQL Server Configuration Manager*
- Go to *SQL Server Network Configuration > Protocols for* <instance_name> *> TCP/IP > Properties*
- In *Protocol tab* change *Enable* to *Yes*
- Go to *IP Address* tab; in *IPAll* (last) section clear *TCP Dynamic Ports* and set *TCP Port* to *1433* (or any other port you want to use)
- Hit *OK* (2x)
- Go to *SQL Server Services* under SQL Server Configuration Manager (on the left side)
- Right click *SQL Server (<instance name>)* and *Restart*

Now SQL server is allowed to accept network connections over the port number 1433. However, your machine is not.

### Firewall
Open up your Firewall's advanced settings. Under Inbound Rules add a New Rule setting the port number to 1433 and connection type to TCP. Dont' change anything else.

### Test
Now you can test your connection from any computer in your network.

    import pymssql
    server = "YOUR-IP-ADDRESS" # i.e. "10.0.2.15"
    username = "databaseUsr"
    password = "D@t@b@$3Pwd"
    dbname   = "DatabaseName"

    conn = pymssql.connect(server, username, password, dbname)
    cursor = conn.cursor()
    cursor.execute("""SELECT * FROM testTable;""")
    data = cursor.fetchall()
    for each in data:
        print("name: %s" % (data[0],))
    conn.close()


Or
    > tsql -H your.ip.add.ress -p 1433 -U username -P password


## Django
Setting up django is even easier.
    
    > git clone https://bitbucket.org/Manfre/django-mssql/
    > cd django-mssql && python3.4 setup.py install && cd ..
    > git clone https://github.com/aaugustin/django-pymssql
    > cd django-pymssql && python3.4 setup.py install && cd ..

Go to your project and edit *settings.py* file
    
    DATABASES = {
        'default': {
            'ENGINE': 'sqlserver_pymssql',
            'HOST':   'your.ip.add.ress',
            'NAME':   'DatabaseName',
            'USER':   'databaseUsr',
            'PASSWORD': 'D@t@b@$3Pwd',
        },
    }


Now your Django + SQL Server app is good to go (don't forget to migrate though)
