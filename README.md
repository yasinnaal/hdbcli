# Introducing hdbcli SAP HANA Python Client
###### Connecting SAP HANA DB using Python

![](https://github.com/yasinnaal/hdbcli/blob/main/doc-img/logo-sap.png)


The SAP HANA client supports Python 3.4 and later and Python 2.7.

The Python Database API Specification v2.0 (PEP 249) defines a set of methods that provides a consistent database interface independent of the actual database being used. The Python extension module for SAP HANA implements PEP 249. Once you install the module, you can access and change the information in databases from Python. In PEP 249, autocommit is turned off by default. In the SAP HANA Python driver, autocommit is turned on by default.

# Install the Python Driver
###### use the Python driver to connect to an SAP HANA database.
Install the Python driver into your local Python environment by using the pip installer so that you can use the Python driver to connect to an SAP HANA database.

# Prerequisites
You have run the SAP HANA client install.

# Procedure
1) If you have multiple Python environments, then activate the Python environment where you want to install the Python driver. If you don’t have multiple Python environments, then ignore this step.
2) Run the install:


## Microsoft Windows	

pip install
```
pip install "C:\Program Files\SAP\hdbclient\hdbcli-N.N.N.zip"
```

easy_install
```
easy_install "C:\Program Files\SAP\hdbclient\hdbcli-N.N.N.zip"
```

disutils installer

Unzip hdbcli-N.N.N.zip into a directory, then run:
```
cd hdbcli-N.N.N
```

Lastly, run:

```
setup.py install
```
   

## UNIX, Linux, and macOS
Use one of the following install methods:

pip install
```
pip install /usr/sap/hdbclient/hdbcli-N.N.N.tar.gz
```

easy_install
```
pip install /usr/sap/hdbclient/hdbcli-N.N.N.tar.gz
```

disutils installer
```
tar -xf hdbcli-N.N.N.tar.gz
```

Then run:
```
cd hdbcli-N.N.N
```

Lastly, run:
```
setup.py install
```

For HANA tenant databases, use the port number 3**NN**13 (where NN is the SAP instance number - e.g. 30013).

For HANA system databases in a multitenant system, the port number is 3**NN**13.

For HANA single-tenant databases, the port number is 3**NN**15.

```
from hdbcli import dbapi
conn = dbapi.connect(
    address="<hostname>",
    port=3<NN>MM,
    user="<username>",
    password="<password>"
)
cursor = conn.cursor()
```

Author: SAP SE
Maintainers: SAP
License: Other/Proprietary License (SAP DEVELOPER LICENSE AGREEMENT)

References:

[Python hdbcli](https://pypi.org/project/hdbcli/)

[SAP Note 3136015](https://help.sap.com/docs/link-disclaimer?site=https://launchpad.support.sap.com/#/notes/3136015)

Thanks.








