Collaborative IaaS with Docker
==============================

[![Stories in Ready](https://badge.waffle.io/EudesRobin/iaas-collaboratif.png?label=ready&title=Ready)](https://waffle.io/EudesRobin/iaas-collaboratif)

**Authors :** 
Alan DAMOTTE, Robin EUDES, Romain BARTHELEMY, Malek MAMMAR, Kai GUO


----------
> The objective of this project is to allow a user group (member) to pool their laptops or desktop in order to calculate big data of few users. To do so, the solution should work with Docker to virtualize user machines and control the use of resources of each machine.

> This branch is dedicated to the frontend side.
----------

How to use it ?
---------------
    .
    ├── LICENCE.md
    ├── meteor-frontend
    ├── README.html
    ├── README.md
    └── scripts

**scripts :**
A folder where you will find few bash scripts to setup/start/stop meteor, start the project, and some others stuffs. A more detailed README.md file in this folder will explain how to use them.

**meteor-frontend :**
This folder contains the meteor projet, the webui. A more detailed README.md file in this folder will explain a bit this webui.


    You must create a file "settings.json" in the following directory : /meteor-frontend
    with this content :
    {
        "rabbitmq": {
                "user": "username_rabbit",
                "password": "password_rabbit",
                "host": "url_rabbit",
                "port": "5672"
        }
    }
    
    Here, it's used by meteor to process received messages (publish by coordinators).
    Be aware that an indentical file must be created in docker/coordinator/publisher  directory (on provider, it's used by coordinator to publish messages )

Links
-------
[Documentation](http://air.imag.fr/index.php/Projets-2015-2016-IaaS_Docker)

[Kanban - Waffle](https://waffle.io/EudesRobin/iaas-collaboratif)

License
-------
[GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.fr.html)
