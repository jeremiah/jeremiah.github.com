---
layout: default
---

## Fun with the Intel® NUC Kit NUC8i7HNK
Oh boy. A core i7 8th generation Hades Canyon NUC. The skull . . . it glows!
![The skull . . . it glows!]({{ "/assets/skull.png" }})

I've purchased Intel's new 800P Optane M.2 memory as an SSD and 32
gigs of DDR4 memory. Hopefully this little beastie will fly.

## Recent talks
I recently [spoke at LibrePlanet](https://media.libreplanet.org/u/libreplanet/m/freedom-embedded-vehicles/).
LibrePlanet is a great conference, I saw a lot of cool talks and met
some great people. I'm embarrassed to say that this is the first time
I've been to LP and it has been going on for ten years. It was great
to get to go inside the Frank Gehry designed Stata Center at MIT.

There is something really wrong with my presentations. I think I try
too hard to be entertaining, I ramble and speak too quickly.

I also spoke at the Software Freedom Law Center on how [car companies
are becoming software
companies](https://downloads.softwarefreedom.org/2018/automotive/1d-foster.webm). There
were a number of other's who spoke, like Mark Shuttleworth and Leilani
Gilpin who's talk was excellent.

## Installing Fossology
Fossology is an open source tool for checking source code and
licensing of software. It's actually free software, or at least part
of it is since at least some of it, if not all of it, is [licensed
under the GPLv2.](https://github.com/fossology/fossology/blob/master/COPYING)

It has some runtime requirements, as of this writing they are;
- PHP versions 5.5.9 to 5.6.x (supported versions)
- Postgresql as database server
- Apache httpd 2.4 as web server.

"These and more dependencies are installed by `utils/fo-installdeps`."
Well, that's convenient, but it would be more convenient if the [debs
of Fossology](https://mirrors.kernel.org/fossology/releases/3.0.0/)
were kept up to date, but you can't have everything.

I opted to use the script to see how that goes. The script is written in 
bash thankfully and at the end of copious (and I do mean copious) packages being installed, it said:
```
run ./../src/demomod/mod_deps to install dependencies
run ./../src/buckets/mod_deps to install dependencies
``` 

Unfortunately, it is not entirely clear whether these are optional or
not. Look at the first one, src/demomod, it looks like it is a
demonstration pacakge for installing a Fossology module. I decided to
skip running those two commands. 

Instead, I jumped ahead and did the familiar;

```
make
sudo make install
```

Then I switched to the /usr/local/lib/fossology/ dir and ran;
```
sudo ./fo-postinstall
```

Oh. That goes ahead and creates a database for me, aomong other
things. I took a look at /usr/local/lib/fossology/fossologyinit.sql to
see what was happening.

This flew by, will take a look at it later;
"NOTE: Running the PostgreSQL vacuum and analyze command can result in a large database performance improvement.  We suggest that you either configure postgres to run its autovacuum and autoanalyze daemons, or maintagent -D in a cron job, or run Admin > Maintenance on a regular basis.  Admin > Dashboard will show you the last time vacuum and analyze have been run."

Then the next steps are;

6. Login to FOSSology with the default fossy/fossy user and password and:

   1.  create yourself a user with administrative privileges
   2.  change the default password for user fossy

This didn't work for me. Instead I changed to the postgres user and just did;
```
$ psql
```
Which put me in the postgres database. I found this quite useful: 
https://www.postgresql.org/docs/9.6/static/auth-pg-hba-conf.html

