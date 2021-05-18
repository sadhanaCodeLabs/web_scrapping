# Data Scrapping/Crawler

Scrapping web content using python scrapy. In this project I scrapped amazon best selling video games.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Python 3.6.0 or higher, I have not tested in previous version of python
Dependency lib's are added into requirement.txt, run dependency.txt to install required python packages.



### Installing and running

A step by step series of examples that tell you how to get a development env running

Install dependency packages 

```
1. python: pip install scrapy 
   install this package with conda run one of the following:
    conda install -c conda-forge scrapy
2. Create python project uisng scrapy
    scrapy startproject web_scrapping
3. Create spiders
    scrapy genspider amazon_bestseller https://www.amazon.com/Best-Sellers-Electronics/zgbs/electronics

```
### Running

```
run python script ./web_scrapping/web_scrapping/controllers/amazon_scrapper.py

csv will be generated under ./web_scrapping/output folder of your current directory. See below for the program console output
```

## Author

* **Sadhana Srivastava**



## Program out

```
csv out file generated under ./web_scrapping/output/

INFO: Overridden settings:
{'AUTOTHROTTLE_TARGET_CONCURRENCY': 0.25,
 'CONCURRENT_REQUESTS': 1,
 'DOWNLOAD_DELAY': 10,
 'NEWSPIDER_MODULE': 'web_scrapping.spiders',
 'ROBOTSTXT_OBEY': True,
 'SPIDER_MODULES': ['web_scrapping.spiders'],
 'USER_AGENT': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 '
               '(KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36'}
2021-05-17 21:25:41 [scrapy.extensions.telnet] INFO: Telnet Password: 768801f8d42be1fd
2021-05-17 21:25:41 [py.warnings] WARNING: /Users/atulsaxena/Downloads/web_scrapping/venv/lib/python3.9/site-packages/scrapy/extensions/feedexport.py:247: ScrapyDeprecationWarning: The `FEED_URI` and `FEED_FORMAT` settings have been deprecated in favor of the `FEEDS` setting. Please see the `FEEDS` setting docs for more details
  exporter = cls(crawler)

2021-05-17 21:25:41 [scrapy.middleware] INFO: Enabled extensions:
['scrapy.extensions.corestats.CoreStats',
 'scrapy.extensions.telnet.TelnetConsole',
 'scrapy.extensions.memusage.MemoryUsage',
 'scrapy.extensions.feedexport.FeedExporter',
 'scrapy.extensions.logstats.LogStats']
2021-05-17 21:25:41 [scrapy.middleware] INFO: Enabled downloader middlewares:
['scrapy.downloadermiddlewares.robotstxt.RobotsTxtMiddleware',
 'scrapy.downloadermiddlewares.httpauth.HttpAuthMiddleware',
 'scrapy.downloadermiddlewares.downloadtimeout.DownloadTimeoutMiddleware',
 'scrapy.downloadermiddlewares.defaultheaders.DefaultHeadersMiddleware',
 'scrapy.downloadermiddlewares.useragent.UserAgentMiddleware',
 'scrapy.downloadermiddlewares.retry.RetryMiddleware',
 'scrapy.downloadermiddlewares.redirect.MetaRefreshMiddleware',
 'scrapy.downloadermiddlewares.httpcompression.HttpCompressionMiddleware',
 'scrapy.downloadermiddlewares.redirect.RedirectMiddleware',
 'scrapy.downloadermiddlewares.cookies.CookiesMiddleware',
 'scrapy.downloadermiddlewares.httpproxy.HttpProxyMiddleware',
 'scrapy.downloadermiddlewares.stats.DownloaderStats']
2021-05-17 21:25:41 [scrapy.middleware] INFO: Enabled spider middlewares:
['scrapy.spidermiddlewares.httperror.HttpErrorMiddleware',
 'scrapy.spidermiddlewares.offsite.OffsiteMiddleware',
 'scrapy.spidermiddlewares.referer.RefererMiddleware',
 'scrapy.spidermiddlewares.urllength.UrlLengthMiddleware',
 'scrapy.spidermiddlewares.depth.DepthMiddleware']
2021-05-17 21:25:41 [scrapy.middleware] INFO: Enabled item pipelines:
[]
2021-05-17 21:25:41 [scrapy.core.engine] INFO: Spider opened
2021-05-17 21:25:41 [scrapy.extensions.logstats] INFO: Crawled 0 pages (at 0 pages/min), scraped 0 items (at 0 items/min)
2021-05-17 21:25:41 [scrapy.extensions.telnet] INFO: Telnet console listening on 127.0.0.1:6023
2021-05-17 21:25:42 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://www.amazon.com/robots.txt> (referer: None)
2021-05-17 21:25:58 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0> (referer: None)
2021-05-17 21:25:58 [amazon_bestseller_video_games] INFO: amazon_bestseller_video_games spider parsing  on https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#1', 'item_name': '$10 PlayStation Store Gift Card [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '225,007', 'price': '$10.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#2', 'item_name': '$10 Xbox Gift Card [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '112,771', 'price': '$10.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#3', 'item_name': '$10 Nintendo eShop Gift Card [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '64,736', 'price': '$5.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#4', 'item_name': 'Roblox Gift Card - 800 Robux [Includes Exclusive Virtual Item] [Online Game Code]', 'star_rating': '4.6 out of 5 stars', 'review_count': '65,593', 'price': '$10.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#5', 'item_name': 'PlayStation DualSense Wireless Controller – Midnight Black', 'star_rating': '4.8 out of 5 stars', 'review_count': '22,972', 'price': '$69.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#6', 'item_name': 'Roblox Gift Card - 2000 Robux [Includes Exclusive Virtual Item] [Online Game Code]', 'star_rating': '4.6 out of 5 stars', 'review_count': '65,593', 'price': '$25.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#7', 'item_name': 'PlayStation Plus: 1 Month Membership [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '25,982', 'price': '$9.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#8', 'item_name': 'PlayStation DualSense Wireless Controller – Cosmic Red', 'star_rating': '4.8 out of 5 stars', 'review_count': '22,972', 'price': '$74.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#9', 'item_name': 'BENGOO G9000 Stereo Gaming Headset for PS4 PC Xbox One PS5 Controller, Noise Cancelling Over Ear Headphones with Mic, LED Light, Bass Surround, Soft Memory Earmuffs for Laptop Mac Nintendo NES Games', 'star_rating': '4.4 out of 5 stars', 'review_count': '76,795', 'price': '$19.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#10', 'item_name': 'SanDisk 128GB microSDXC Card, Licensed for Nintendo Switch - SDSQXAO-128G-GNCZN', 'star_rating': '4.9 out of 5 stars', 'review_count': '125,981', 'price': '$23.50'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#11', 'item_name': 'New Pokémon Snap - Nintendo Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '803', 'price': '$59.07'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#12', 'item_name': '$20 Xbox Gift Card [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '112,771', 'price': '$20.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#13', 'item_name': 'Nintendo Switch Pro Controller', 'star_rating': '4.9 out of 5 stars', 'review_count': '47,080', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#14', 'item_name': "Super Mario 3D World + Bowser's Fury - Nintendo Switch", 'star_rating': '4.9 out of 5 stars', 'review_count': '13,115', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#15', 'item_name': 'Mass Effect Legendary Edition - PlayStation 4', 'star_rating': '4.3 out of 5 stars', 'review_count': '25', 'price': '$59.88'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#16', 'item_name': 'Gaming Headset with Mic for PS5, PS4, Xbox, Nintendo Switch and PC, NexiGo Over-Ear Headphones, Skin-Friendly Earmuffs, Lightweight and Breathable, Multi-Platform, White', 'star_rating': '4.1 out of 5 stars', 'review_count': '66', 'price': '$19.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#17', 'item_name': 'Animal Crossing: New Horizons - Nintendo Switch', 'star_rating': '4.9 out of 5 stars', 'review_count': '49,615', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#18', 'item_name': 'Playstation DualSense Charging Station', 'star_rating': '4.9 out of 5 stars', 'review_count': '4,309', 'price': '$29.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#19', 'item_name': 'Playstation DualSense Wireless Controller', 'star_rating': '4.8 out of 5 stars', 'review_count': '22,972', 'price': '$69.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#20', 'item_name': 'amFilm Tempered Glass Screen Protector for Nintendo Switch 2017 (2-Pack)', 'star_rating': '4.8 out of 5 stars', 'review_count': '84,335', 'price': '$5.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#21', 'item_name': 'Story of Seasons: Friends of Mineral Town - Nintendo Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '4,167', 'price': '$19.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#22', 'item_name': 'RUNMUS Gaming Headset Xbox One Headset with 7.1 Surround Sound Stereo, PS4 Headset with Noise Canceling Mic & LED Light, Compatible with PC, PS4, Xbox One Controller(Adapter Needed), Nintendo Switch', 'star_rating': '4.4 out of 5 stars', 'review_count': '83,488', 'price': '$19.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#23', 'item_name': 'Roblox Gift Card - 4500 Robux [Includes Exclusive Virtual Item] [Online Game Code]', 'star_rating': '4.6 out of 5 stars', 'review_count': '65,593', 'price': '$44.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#24', 'item_name': 'Xbox Wireless Controller – Electric Volt for Xbox Series X|S, Xbox One, and Windows 10 Devices', 'star_rating': '5.0 out of 5 stars', 'review_count': '3', 'price': '$59.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#25', 'item_name': 'Logitech G502 HERO High Performance Wired Gaming Mouse, HERO 25K Sensor, 25,600 DPI, RGB, Adjustable Weights, 11 Programmable Buttons, On-Board Memory, PC / Mac', 'star_rating': '4.7 out of 5 stars', 'review_count': '18,097', 'price': '$46.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#26', 'item_name': 'The Legend of Zelda: Breath of the Wild - Nintendo Switch', 'star_rating': '4.9 out of 5 stars', 'review_count': '36,876', 'price': '$47.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#27', 'item_name': 'Mario Golf: Super Rush - Nintendo Switch', 'star_rating': None, 'review_count': None, 'price': '$59.88'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#28', 'item_name': 'Miitopia - Nintendo Switch', 'star_rating': None, 'review_count': None, 'price': '$49.88'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#29', 'item_name': 'Nintendo Switch with Gray Joy‑Con -\xa0HAC-001(-01)', 'star_rating': '4.9 out of 5 stars', 'review_count': '78,602', 'price': '$349.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#30', 'item_name': 'PowerA USB Charging Cable for PlayStation 4', 'star_rating': '4.6 out of 5 stars', 'review_count': '22,203', 'price': '$6.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#31', 'item_name': 'Mario Kart 8 Deluxe - Nintendo Switch', 'star_rating': '4.9 out of 5 stars', 'review_count': '47,734', 'price': '$49.94'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#32', 'item_name': 'Controller Battery Pack for Xbox One/Xbox Series X|S, BEBONCOOL 2x2550 mAh Rechargeable Battery Pack for Xbox Series X|S/Xbox One/Xbox One S/Xbox One X/Xbox One Elite Controller-Green', 'star_rating': '4.8 out of 5 stars', 'review_count': '29,782', 'price': '$19.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#33', 'item_name': 'Minecraft: Java Edition for PC/Mac [Online Game Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '25,087', 'price': '$26.95'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#34', 'item_name': 'Ring Fit Adventure - Nintendo Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '20,877', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#35', 'item_name': 'Nintendo Blue/ Neon Yellow Joy-Con (L-R) - Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '63,392', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#36', 'item_name': 'Nintendo Neon Purple/ Neon Orange Joy-Con (L-R) - Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '63,392', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#37', 'item_name': 'Redragon S101 Wired Gaming Keyboard and Mouse Combo RGB Backlit Gaming Keyboard with Multimedia Keys Wrist Rest and Red Backlit Gaming Mouse 3200 DPI for Windows PC Gamers (Black)', 'star_rating': '4.6 out of 5 stars', 'review_count': '28,830', 'price': '$33.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#38', 'item_name': 'Logitech G305 LIGHSTPEED Wireless Gaming Mouse, Hero 12K Sensor, 12,000 DPI, Lightweight, 6 Programmable Buttons, 250h Battery Life, On-Board Memory, PC/Mac - Black', 'star_rating': '4.7 out of 5 stars', 'review_count': '4,103', 'price': '$39.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#39', 'item_name': 'Nintendo Switch - Animal Crossing: New Horizons Edition - Switch', 'star_rating': '4.9 out of 5 stars', 'review_count': '78,602', 'price': '$299.00'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#40', 'item_name': 'PlayStation Plus: 12 Month Membership [Digital Code]', 'star_rating': '4.8 out of 5 stars', 'review_count': '43,226', 'price': '$59.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#41', 'item_name': 'Sony PULSE 3D Wireless Headset', 'star_rating': '4.7 out of 5 stars', 'review_count': '5,948', 'price': '$99.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#42', 'item_name': 'Jeecoo Xiberia USB Pro Gaming Headset for PC- 7.1 Surround Sound Headphones with Noise Cancelling Microphone- Memory Foam Ear Pads RGB Lights for Laptops', 'star_rating': '4.4 out of 5 stars', 'review_count': '15,534', 'price': '$27.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#43', 'item_name': 'Mass Effect Legendary Edition - Xbox One', 'star_rating': '4.5 out of 5 stars', 'review_count': '11', 'price': '$59.88'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#44', 'item_name': 'Hestia Goods Switch Carrying Case for Nintendo Switch, with 20 Games Cartridges Protective Hard Shell Travel Carrying Case Pouch for Nintendo Switch Console & Accessories, Black', 'star_rating': '4.8 out of 5 stars', 'review_count': '13,941', 'price': '$11.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#45', 'item_name': 'Super Smash Bros. Ultimate - Nintendo Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '47,441', 'price': None}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#46', 'item_name': 'BEBONCOOL PS4 Controller Charger, Controller USB Charging Station Dock for DualShock 4, For PlayStation 4 Charging Station for Playstation4 / PS4 / PS4 Slim / PS4 Pro Controller-Black', 'star_rating': '4.7 out of 5 stars', 'review_count': '39,969', 'price': '$14.98'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#47', 'item_name': 'Just Dance 2021 - Nintendo Switch Standard Edition', 'star_rating': '4.8 out of 5 stars', 'review_count': '18,225', 'price': '$30.56'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#48', 'item_name': 'Final Fantasy XIV Online: 60 Day Time Card [Online Game Code]', 'star_rating': '4.8 out of 5 stars', 'review_count': '3,721', 'price': '$29.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#49', 'item_name': 'PICTEK Gaming Mouse Wired [7200 DPI] [Programmable] [Breathing Light] Ergonomic Game USB Computer Mice RGB Gamer Desktop Laptop PC Gaming Mouse, 7 Buttons for Windows 7/8/10/XP Vista Linux, Black', 'star_rating': '4.6 out of 5 stars', 'review_count': '1,082', 'price': '$13.99'}
2021-05-17 21:25:58 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0>
{'ranking': '#50', 'item_name': 'Xbox Game Pass Ultimate: 1 Month Membership [Digital Code]', 'star_rating': '4.8 out of 5 stars', 'review_count': '14,665', 'price': '$14.99'}
2021-05-17 21:25:58 [amazon_bestseller_video_games] INFO: following to next page: https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2
2021-05-17 21:26:12 [scrapy.core.engine] DEBUG: Crawled (200) <GET https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2> (referer: https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_nav_0)
2021-05-17 21:26:12 [amazon_bestseller_video_games] INFO: amazon_bestseller_video_games spider parsing  on https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#51', 'item_name': 'Charger for Nintendo Switch, AC Adapter for Nintendo Switch - Fast Travel Wall Charger with 5FT USB Type C Cable 15V/2.6A Power Supply for Nintendo Switch Supports TV Mode and Dock Station', 'star_rating': '4.7 out of 5 stars', 'review_count': '4,070', 'price': '$16.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#52', 'item_name': 'Razer Viper Mini Ultralight Gaming Mouse: Fastest Gaming Switches - 8500 DPI Optical Sensor - Chroma RGB Underglow Lighting - 6 Programmable Buttons - Drag-Free Cord - Classic Black', 'star_rating': '4.7 out of 5 stars', 'review_count': '13,478', 'price': '$29.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#53', 'item_name': 'Redragon K552 Mechanical Gaming Keyboard RGB LED Rainbow Backlit Wired Keyboard with Red Switches for Windows Gaming PC (87 Keys, Black)', 'star_rating': '4.4 out of 5 stars', 'review_count': '24,341', 'price': '$31.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#54', 'item_name': 'Apex Legends - 1,000 Apex Coins [Online Game Code]', 'star_rating': '3.9 out of 5 stars', 'review_count': '1,082', 'price': '$9.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#55', 'item_name': '[3 Pack] Hestia Goods Tempered Glass Screen Protector for Nintendo switch - Transparent HD Clear Anti-Scratch Screen Protector for Nintendo Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '14,659', 'price': '$5.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#56', 'item_name': 'SanDisk 256GB microSDXC Card, Licensed for Nintendo Switch - SDSQXAO-256G-GNCZN', 'star_rating': '4.9 out of 5 stars', 'review_count': '125,981', 'price': '$45.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#57', 'item_name': 'YCCTEAM Wireless Game Controller Compatible with PS-4 Console/iOS 13 /Android 10 /MAC/PC (White)', 'star_rating': '3.8 out of 5 stars', 'review_count': '4,086', 'price': '$31.95'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#58', 'item_name': 'Hori Nintendo Switch Split Pad Pro (Red) Ergonomic Controller for Handheld Mode - Officially Licensed By Nintendo - Nintendo Switch', 'star_rating': '4.6 out of 5 stars', 'review_count': '15,886', 'price': '$38.20'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#59', 'item_name': 'Nintendo Switch with Neon Blue and Neon Red Joy‑Con - HAC-001(-01)', 'star_rating': '4.9 out of 5 stars', 'review_count': '78,602', 'price': '$364.75'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#60', 'item_name': 'VALORANT $25 Gift Card - PC [Online Game Code]', 'star_rating': '4.6 out of 5 stars', 'review_count': '3,202', 'price': '$25.00'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#61', 'item_name': 'Razer Kraken X Ultralight Gaming Headset: 7.1 Surround Sound - Lightweight Aluminum Frame - Bendable Cardioid Microphone - PC, PS4, PS5, Switch, Xbox One, Xbox Series X & S, Mobile - Black', 'star_rating': '4.4 out of 5 stars', 'review_count': '14,940', 'price': '$49.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#62', 'item_name': 'Kandagawa Jet Girls - Racing Hearts Edition (Day 1) - PlayStation 4', 'star_rating': '4.8 out of 5 stars', 'review_count': '471', 'price': '$60.49'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#63', 'item_name': 'VALORANT $10 Gift Card - PC [Online Game Code]', 'star_rating': '4.6 out of 5 stars', 'review_count': '3,202', 'price': '$10.00'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#64', 'item_name': 'Playstation Plus: 3 Month Membership [Digital Code]', 'star_rating': '4.8 out of 5 stars', 'review_count': '14,366', 'price': '$24.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#65', 'item_name': 'FIFA 20 Ultimate Team Points 100 [Online Game Code]', 'star_rating': '2.3 out of 5 stars', 'review_count': '5', 'price': '$0.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#66', 'item_name': 'NPET K10 Gaming Keyboard USB Wired Floating Keyboard, Quiet Ergonomic Water-Resistant Mechanical Feeling Keyboard, Ultra-Slim Rainbow LED Backlit Keyboard for Desktop, Computer, PC', 'star_rating': '4.6 out of 5 stars', 'review_count': '13,002', 'price': '$14.45'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#67', 'item_name': '[3 Pack] Screen Protector Tempered Glass for Nintendo Switch, iVoler Transparent HD Clear Anti-Scratch Screen Protector Compatible Nintendo Switch', 'star_rating': '4.8 out of 5 stars', 'review_count': '26,465', 'price': '$6.95'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#68', 'item_name': 'Xbox Wireless Controller - Shock Blue', 'star_rating': '4.7 out of 5 stars', 'review_count': '8,379', 'price': '$59.00'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#69', 'item_name': 'PowerA Spectra Enhanced Illuminated Wired Controller for Xbox One, gamepad, wired video game controller, gaming controller, Xbox One, works with Xbox Series X|S', 'star_rating': '4.4 out of 5 stars', 'review_count': '19,067', 'price': '$39.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#70', 'item_name': 'Xbox Game Pass Ultimate: 3 Month Membership [Digital Code]', 'star_rating': '4.8 out of 5 stars', 'review_count': '14,665', 'price': '$39.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#71', 'item_name': 'Turtle Beach Ear Force Recon 50x Stereo Gaming Headset for Xbox One & Xbox Series X|S (Compatible with Xbox controller with 3.5mm Headset Jack) PlayStation 5 & PS4', 'star_rating': '4.4 out of 5 stars', 'review_count': '30,319', 'price': '$24.95'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#72', 'item_name': "Luigi's Mansion 3 - Nintendo Switch", 'star_rating': '4.8 out of 5 stars', 'review_count': '21,346', 'price': None}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#73', 'item_name': 'UGREEN Ethernet Adapter USB 2.0 to 10 100 Network RJ45 LAN Wired Adapter Compatible for Nintendo Switch Wii Wii U MacBook Chromebook Windows Mac OS Surface Linux ASIX AX88772 Chipset Black', 'star_rating': '4.6 out of 5 stars', 'review_count': '18,219', 'price': '$9.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#74', 'item_name': 'Gaming headset for PS4 Xbox one PS5 controller, Beexcellent Newest Deep Bass Stereo Sound Over Ear Headphone with Noise Isolation LED Light for PC Laptop Tablet Mac (Blue)', 'star_rating': '4.5 out of 5 stars', 'review_count': '29,995', 'price': '$15.56'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#75', 'item_name': 'Titanfall 2: Ultimate Edition - Xbox One [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '300', 'price': '$2.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#76', 'item_name': 'PowerA FUSION Pro Wired Controller for Xbox One - Black, Gamepad, Wired Video Game Controller, Gaming Controller, Xbox One, Works with Xbox Series X|S', 'star_rating': '4.5 out of 5 stars', 'review_count': '8,400', 'price': '$60.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#77', 'item_name': 'Ratchet & Clank: Rift Apart Launch Edition - Playstation 5', 'star_rating': None, 'review_count': None, 'price': '$69.88'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#78', 'item_name': 'KontrolFreek FPS Freek Galaxy Purple for PlayStation 4 (PS4) and PlayStation 5 (PS5) | Performance Thumbsticks | 1 High-Rise, 1 Mid-Rise | Purple', 'star_rating': '4.6 out of 5 stars', 'review_count': '15,758', 'price': '$14.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#79', 'item_name': 'Oculus Quest 2 Elite Strap for Enhanced Support and Comfort in VR', 'star_rating': '4.3 out of 5 stars', 'review_count': '6,370', 'price': '$49.00'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#80', 'item_name': 'MOVONE Wireless Controller Dual Vibration Game Joystick Controller for PS4/ Slim/Pro,Compatible with PS4 Console (White+Black)', 'star_rating': '3.8 out of 5 stars', 'review_count': '868', 'price': '$29.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#81', 'item_name': 'Mass Effect Legendary - Xbox Series X [Digital Code]', 'star_rating': '5.0 out of 5 stars', 'review_count': '2', 'price': '$59.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#82', 'item_name': 'League of Legends $10 Gift Card - NA Server Only [Online Game Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '5,585', 'price': '$10.00'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#83', 'item_name': 'BENGOO KM-1 Wireless Gaming Mouse, Computer Mouse with Honeycomb Shell, 6 Programmed Buttons, 3 Adjustable DPI, Silent Click, USB Receiver, Ergonomic RGB Optical Gamer Mice Mouse for Laptop PC Mac', 'star_rating': '4.4 out of 5 stars', 'review_count': '1,545', 'price': '$24.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#84', 'item_name': 'Logitech G600 MMO Gaming Mouse, RGB Backlit, 20 Programmable Buttons', 'star_rating': '4.5 out of 5 stars', 'review_count': '10,852', 'price': '$31.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#85', 'item_name': 'Logitech G Pro Wireless Gaming Mouse with Esports Grade Performance', 'star_rating': '4.7 out of 5 stars', 'review_count': '6,413', 'price': '$113.49'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#86', 'item_name': 'PS4 Controller Charger Charging Cable 10ft 2 Pack Nylon Braided Extra Long Micro USB 2.0 High Speed Data Sync Cord Compatible for Playstaion 4, PS4 Slim/Pro, Xbox One S/X Controller, Android Phones', 'star_rating': '4.6 out of 5 stars', 'review_count': '7,170', 'price': '$9.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#87', 'item_name': 'Biomutant - PlayStation 4 Standard Edition', 'star_rating': None, 'review_count': None, 'price': '$59.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#88', 'item_name': 'Minecraft (Nintendo Switch)', 'star_rating': '4.8 out of 5 stars', 'review_count': '20,858', 'price': '$33.50'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#89', 'item_name': 'Super Mario Party', 'star_rating': '4.8 out of 5 stars', 'review_count': '19,002', 'price': '$55.95'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#90', 'item_name': 'Nintendo Switch Online 12-Month Individual Membership [Digital Code]', 'star_rating': '4.8 out of 5 stars', 'review_count': '14,794', 'price': '$19.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#91', 'item_name': 'Xbox Live Gold: 3 Month Membership [Digital Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '65,033', 'price': '$24.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#92', 'item_name': 'AC Power Cord Compatible Xbox One S, Xbox One X, Xbox Series X / S, Sony PS3 / PS4 / PS5 Playstation 4 Slim, PSP, PSV Supply Cable Replacement', 'star_rating': '4.8 out of 5 stars', 'review_count': '5,587', 'price': '$8.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#93', 'item_name': 'League of Legends $25 Gift Card - NA Server Only [Online Game Code]', 'star_rating': '4.7 out of 5 stars', 'review_count': '5,585', 'price': '$25.00'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#94', 'item_name': 'Razer DeathAdder Essential Gaming Mouse: 6400 DPI Optical Sensor - 5 Programmable Buttons - Mechanical Switches - Rubber Side Grips - White', 'star_rating': '4.7 out of 5 stars', 'review_count': '25,548', 'price': '$29.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#95', 'item_name': 'DualShock 4 Back Button Attachment - PlayStation 4', 'star_rating': '4.6 out of 5 stars', 'review_count': '8,471', 'price': '$19.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#96', 'item_name': 'iVoler Carrying Storage Case for Nintendo Switch, Portable Travel All Protective Hard Messenger Bag Soft Lining 18 Games for Switch Console Pro Controller & Accessories Black', 'star_rating': '4.8 out of 5 stars', 'review_count': '9,389', 'price': '$23.79'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#97', 'item_name': 'Xbox Series S', 'star_rating': '4.7 out of 5 stars', 'review_count': '3,224', 'price': None}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#98', 'item_name': 'Quest Link Cable 16ft, VOKOO Oculus Quest Link Cable, High Speed Data Transfer & Fast Charging USB C Cable Compatible for Oculus Quest Headset and Gaming PC', 'star_rating': '4.3 out of 5 stars', 'review_count': '3,742', 'price': '$29.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#99', 'item_name': 'Tomee AC Adapter for New Nintendo 3DS/ New Nintendo 2DS XL/ New Nintendo 3DS/ New Nintendo 3DS XL/ Nintendo 2DS/ Nintendo 3DS XL/ Nintendo 3DS/ Nintendo DSi XL/ Nintendo Dsi', 'star_rating': '4.7 out of 5 stars', 'review_count': '8,597', 'price': '$4.99'}
2021-05-17 21:26:12 [scrapy.core.scraper] DEBUG: Scraped from <200 https://www.amazon.com/best-sellers-video-games/zgbs/videogames/ref=zg_bs_pg_2/132-7567701-7319250?_encoding=UTF8&pg=2>
{'ranking': '#100', 'item_name': 'HyperX Cloud Stinger – Gaming Headset, Lightweight, Comfortable Memory Foam, Swivel to Mute Noise-Cancellation Microphone, Works on PC, PS4, PS5, Xbox One, Xbox Series X|S, Nintendo Switch and Mobile', 'star_rating': '4.4 out of 5 stars', 'review_count': '22,459', 'price': '$40.99'}
2021-05-17 21:26:12 [scrapy.core.engine] INFO: Closing spider (finished)
2021-05-17 21:26:12 [scrapy.extensions.feedexport] INFO: Stored csv feed (100 items) in: output/amazon_bestseller_video_games_2021-05-18T01-25-41.csv
2021-05-17 21:26:12 [scrapy.statscollectors] INFO: Dumping Scrapy stats:
{'downloader/request_bytes': 1221,
 'downloader/request_count': 3,
 'downloader/request_method_count/GET': 3,
 'downloader/response_bytes': 164139,
 'downloader/response_count': 3,
 'downloader/response_status_count/200': 3,
 'elapsed_time_seconds': 30.785065,
 'feedexport/success_count/FileFeedStorage': 1,
 'finish_reason': 'finished',
 'finish_time': datetime.datetime(2021, 5, 18, 1, 26, 12, 698193),
 'httpcompression/response_bytes': 667140,
 'httpcompression/response_count': 2,
 'item_scraped_count': 100,
 'log_count/DEBUG': 103,
 'log_count/INFO': 14,
 'log_count/WARNING': 1,
 'memusage/max': 52002816,
 'memusage/startup': 52002816,
 'request_depth_max': 1,
 'response_received_count': 3,
 'robotstxt/request_count': 1,
 'robotstxt/response_count': 1,
 'robotstxt/response_status_count/200': 1,
 'scheduler/dequeued': 2,
 'scheduler/dequeued/memory': 2,
 'scheduler/enqueued': 2,
 'scheduler/enqueued/memory': 2,
 'start_time': datetime.datetime(2021, 5, 18, 1, 25, 41, 913128)}
2021-05-17 21:26:12 [scrapy.core.engine] INFO: Spider closed (finished)

Process finished with exit code 0
    
```
