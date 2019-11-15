# Pixiv Dataset Overview

This repository is for releasing two pixiv related datasets, both originally used for training neural network models for *sketch colorization* task. 

**Note: This repo is quite old and some of the ids provided may be obsolete. e.g. 18539562,18445616 ; 18472825,18464499. Please use with caution.** (Thanks to Shuchita who pointed this out.)


### File description

##### popular_pixiv_image_ids.txt
There is a total of 268116 ids of popular pixiv image pages collected through the tag "xxx user入り" on pixiv. They were collected from March 4th to March 15th. Each line contains an pixiv image page id.

##### colored_sketch_pair.csv
There are 6192 pairs of colored-sketch image page ids, separated by commas. They were collected by first using the two tags "塗ってみた", "塗らせていただきました". Then I parsed the descriptions of collected images and getting the urls in the descriptions that matches pixiv image pages. I went through them manually one by one to check whether it indeed corresponded to a pair of colored-sketch images. There are still wrong pairs that I missed, but I expect the error rate is below 1%. Please let me know if you find them (email: jerrylijiaming [at] gmail.com).
To my knowledge this should be the only such dataset available.

##### pixiv_bookmark_list.txt
This is the list of pixiv bookmarks I used to scrape the popular pixiv images.

### Example

#### colored_sketch_pair.csv

##### Sketch
![Sketch](https://raw.githubusercontent.com/jerryli27/pixiv_dataset/master/14577906_p0.png "id 14577906")

##### Colored
![Colored](https://raw.githubusercontent.com/jerryli27/pixiv_dataset/master/14646322_p0.jpg "id 14646322")

Both images are cropped and only serve as examples of what the dataset contains. If you want the original image, please follow the download instruction below.

### Download instruction
Unfortunately, we cannot directly provide the images since we do not own them. One can use the PixivUtil2 program (https://github.com/Nandaka/PixivUtil2) to batch download pixiv images given their ids. One can also write their own Pixiv scraper. If you only need a few images, you can usually get them through visiting the corresponding url: https://www.pixiv.net/member_illust.php?mode=medium&illust_id=REPLACE_WITH_ID
Note that each pixiv image page may contain more than one image. Also note that some pages may contain contents not safe for work.

### Why release the data?
I spent lots of times on collecting data and I don't want that to be a barrier to research. I also want more people to get interested in sketch colorization task and AI in general. Here's a related website with demo: http://paintschainer.preferred.tech/index_en.html (Website owned by Preferred Networks).

### License:
MIT
