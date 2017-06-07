# Pixiv Dataset Overview

This repository is for releasing two pixiv related datasets, both originally used for training neural network models for *sketch colorization* task. 


### File description

##### popular_pixiv_image_ids.txt
There is a total of 268116 ids of popular pixiv image pages collected through the tag "xxx user入り" on pixiv. They were collected from March 4th to March 15th. Each line contains an pixiv image page id.

##### colored_sketch_pair.csv
There are 6192 pairs of colored-sketch image page ids, separated by commas. They were collected by first using the two tags "塗ってみた", "塗らせていただきました". Then I parsed the descriptions of collected images and getting the urls in the descriptions that matches pixiv image pages. I went through them manually one by one to check whether it indeed corresponded to a pair of colored-sketch images. There are still wrong pairs that I missed, but I expect the error rate is below 1%. Please let me know if you find them (email: jerrylijiaming [at] gmail.com).

##### pixiv_bookmark_list.txt
This is the list of pixiv bookmarks I used to scrape the popular pixiv images.


### Download instruction
Unfortunately, we cannot directly provide the images since we do not own them. One can use the PixivUtil2 program (https://github.com/Nandaka/PixivUtil2) to batch download pixiv images given their ids. One can also write their own Pixiv scraper. If you only need a few images, you can usually get them through visiting the corresponding url: https://www.pixiv.net/member_illust.php?mode=medium&illust_id=REPLACE_WITH_ID
Note that each pixiv image page may contain more than one image. Also note that some pages may contain contents not safe for work.

### Why release the data?
I spent lots of times on collecting data and I don't want that to be a barrier to research. I also want more people to get interested in sketch colorization task and AI in general. Here's a related website with demo: http://paintschainer.preferred.tech/index_en.html (Website owned by Preferred Networks).

### License:
MIT
