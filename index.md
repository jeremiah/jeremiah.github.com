---
layout: default
---

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

I opted to use the script to see how that goes. 


## Reflections from FOSDEM 2018
Some quick notes on this year's [FOSDEM](https://fosdem.org/2018)

 1. It is as crowded as ever, cramped hallways, long lines for food and
    transport, no seats in the classrooms.
 2. It is as relevant as ever, with a mixed selection of polished,
    professional content and less polished, developer-centric content
    and presentation.
 3. Video capture has been standard for a few years, they've worked
    out some of the kinks and every talk gets coverage. Now they're
    shortening editing times of the videos and making them available
    much more quickly. On the second day of the event there were
    videos already published and there are at least 54 videos ready
    for viewing:
    <https://fosdem.org/2018/news/2018-02-04-first-videos-online/>
    Perhaps more importantly, they now have a stream of the event that
    is available on YouTube;
    https://www.youtube.com/channel/UCYOPCKYceoPwLI-A7tck3wg This
    turns FOSDEM into an entirely different type of event, making the
    person to person contact more valuable.
 4. An alternate take on FOSDEM can be found here: http://n-gate.com/fosdem/2018/01/28/0/

### Videos relevant to work in GENIVI
[OpenADx – xcelerate your Automated Driving development](https://fosdem.org/2018/schedule/event/automated_driving/)
* "Bosch Automated Driving division, together with Microsoft, is
  currently building up an ecosystem of companies within the industry
  including OEMs, tier 1 suppliers, tool vendors, research organisations
  but also partners from other industries like the IT industry. The
  intiative called OpenADx is supported by the Eclipse Foundation as a
  host for the activities."

[War Stories from the Automotive FLOSS Front](https://fosdem.org/2018/schedule/event/automotive_floss/)
* Electrobit comes to FOSDEM. This talk by Susanne
  Oberhauser-Hirschoff and Stefan Potyra was a bit of a dark horse. It
  ended up in the lightning talks instead of the embedded track but I
  think it is important because it seems to echo the experience of
  many companies as they experience open source and automotive worlds
  collide.

[Open-Source Trusted Computing for the IoT](https://fosdem.org/2018/schedule/event/sancus/)
* A researcher from imec-DistriNet, KU Leuven (BE) talks about Trusted computing, particularly for automotive.

[Piece of Cake - testing remote embedded devices made easy with MuxPi](https://fosdem.org/2018/schedule/event/remote_embedded_testing/)
* "Paweł Wieczorek presented a fresh open hardware approach at
  providing remote access (including device flashing, debugging and
  power management) for embedded devices." They've created an open
  hardware board that allows one to remotely reboot and even flash
  hardware - quite useful in distributed teams. 

### Videos of note
[Component Sourcing for Design and Manufacturing in Shenzhen](https://www.youtube.com/watch?v=XwUL6Afo6QQ)
* Short video with details on how to get trustworthy suppliers of PCB components.

[Igniting the Open Hardware Ecosystem with RISC-V](https://video.fosdem.org/2018/K.1.105/riscv.mp4)
* New ISA (Instruction Set Architecture) maintained by a non-profit Foundation.

