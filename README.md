Preview
-------
![](http://www.dorpstraat.com/bitcoin.png)
(image by [wwortel])

# [Bitcointalk Thread](https://bitcointalk.org/index.php?topic=67274.0) #

What is +Coin?
--------------
+Coin is a **Web Interface** built to run on any **PHP web server**, it works with any coin based on **Bitcoin including Litecoin, Namecoin, and many others** -
Installation is done by downloading this repo, and placing it on a PHP web server.

(***there's a download button on the right to get the .zip***, or just clone with git as normal)

**WARNING: +Coin does not have its own authentication security
system, so I recommend that you secure it with an Apache
.htaccess or whatever web server specific security you can use.**


Licensing
---------
+Coin is released under UNLICENSE (Public Domain), this allows
you to use it, edit and claim it as your own, and even sell it
or use it commercially.
NOTE: Bootstrap is under the Apache v2 license, and the JSON-RPC
class used by +Coin is released under the GPL v3. So please be
aware of the restrictions if you do want to use +Coin in any
way that may break the GPL v3 or Apache v2 licensing.

Configuring
-----------
You should be able to simply place your RPC Information for the
daemon you are using in **config.php** (Please **don't** fill in the
MySQL Details, they aren't needed in this version).

    $wallets['wallet 1'] = array("user" => "bitcoinrpc",  
            "pass" =>   "password",      
            "host" =>   "hostname",     
            "port" =>   8332,
			"protocol" => "https"
	);   

You can obtain the RPC Information from:

**Windows**

   - %appdata%\Bitcoin\bitcoin.conf

**Linux**

   - ~/.bitcoin/bitcoin.conf
 
**OSX**

   - ~/Library/Application Support/Bitcoin/bitcoin.conf

wwortel notes:
* this WebUI is geared to the terminology and exchange rate addresses for Bitcoin currency but can be edited to serve other *coin currencies. The Qt graphical interface does not need to be present.
E.g. under Linux the presence and running of bitcoind suffices and the webserver should support PHP and exclusively serve this application via the https protocol as sensitive information is passed between the user and the bitcoin daemon. 

* Do read the file 'SECURITYandCHANGES.txt' !!!! It is absolutely essential to encrypt and protect the communication between the WebUI and where you are on the internet.

* extensions made: 
    * Euro and USD rates on main page,
    * Setting of Transaction Fee on basis of expected waiting time until addition to the block chain,
    * Bug corrections (tests added for array indices that when non-existent would raise errors),
    * Alternative daemon info implementation because of API call 'getinfo' having been deprecated in bitcoind,
    * Link to Debitpay to open in another tab that application to translate bitpay codes to bitcoin addresses.
      Adapt the link at the end of 'header.php' to the url where your instance of DeBitpay is found (source elsewhere on github). 

DONATIONS
---------

Donations are accepted:

- BTC: 1SoMGuYknDgyYypJPVVKE2teHBN4HDAh3
- LTC: LSomguyTSwcw3hZKFts4P453sPfn4Y5Jzv

wwortel:
- BTC: 1LkzWBvy847UNvAcJHjMJJbpHcNY8VnTL
Thank you!
