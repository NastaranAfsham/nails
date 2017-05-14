**Network Analysis Interface for Literature Studies**  
by _[Juho Salminen](https://twitter.com/Juho_Salminen), [Antti Knutas](https://twitter.com/aknutas) and [Arash Hajikhani](https://twitter.com/arash_hajikhani)_  
at _Lappeenranta University of Technology_

## What Is It?
This site shares our experiments and tools for performing statistical and Social Network Analysis (SNA) on citation data. SNA is a new way for researchers to map large datasets and get insights from new angles by analyzing connections between articles. As the amount of publications grows on any given field, automatic tools for this sort of analysis are becoming increasingly important prior to starting research on new fields. _nails_ also provides useful data when performing systematic mapping studies in scientific literature.

The steps for downloading data from [Web of Knowledge](http://webofknowledge.com/) and using our tools to process it are detailed below. The set of tools which are required to perform the analyses are free and need a minimum amount of installation. Furthermore, a web-based analysis server [HAMMER](http://hammer.nailsproject.net/) is available for your use so that you can process the data without needing to do any installation or manual processing steps. Please review the _[How To Use](#how-to-use)_ section below for more information. You can also view a brief [video tutorial](https://youtu.be/I1bRXQs_zMk?list=PLJiFJenPKrLOpdu7E1gEhVEAWF7CLQs_2) on how to get started. There is also a longer [video tutorial series](https://www.youtube.com/playlist?list=PLJiFJenPKrLOpdu7E1gEhVEAWF7CLQs_2) available for more information about the topic.

The project files are available as open source here in our [Github repository](https://github.com/aknutas/nails). If you link or refer to us, please link to our [project page](http://nailsproject.net/).

### Science!
The basic design and bibliometric principles of the system have been published in a research article:

Antti Knutas, Arash Hajikhani, Juho Salminen, Jouni Ikonen, and Jari Porras. 2015. _Cloud-Based Bibliometric Analysis Service for Systematic Mapping Studies_. In Proceedings of the 16th International Conference on Computer Systems and Technologies (CompSysTech '15). DOI: 10.1145/2812428.2812442

A preprint version of the article is [available for download](http://www.codecamp.fi/lib/exe/fetch.php/wiki/nails-compsystech2015-preprint.pdf) as PDF. The official version is now available at the [ACM Digital Library](http://dl.acm.org/citation.cfm?doid=2812428.2812442). If you use the software in your scientific work, please consider citing us.

Some publications that have used our analysis tool:
* Kolle, S. R., Shankarappa, T. H., Manjunatha Reddy, T. B., & Muniyappa, A. (2015). [Scholarly Communication in the International Journal of Pest Management: A Bibliometric Analysis from 2005 to 2014](http://www.tandfonline.com/doi/abs/10.1080/10496505.2015.1087854). Journal of Agricultural & Food Information, 16(4), 301-314.
* Salminen, J. (2015). [The role of collective intelligence in crowdsourcing innovation](http://urn.fi/URN:ISBN:978-952-265-876-0). Acta Universitatis Lappeenrantaensis.
* Geissdoerfer, M., Savaget, P., Bocken, N. M., & Hultink, E. J. (2016). The Circular Economy–A new sustainability paradigm?. Journal of Cleaner Production.
* Kolle, S. R. (2016). [Global research on air pollution between 2005 and 2014: A bibliometric study.](http://www.emeraldinsight.com/doi/full/10.1108/CB-05-2016-0008) Collection Building, 35(3).
* Knutas, A. (2016). Increasing Beneficial Interactions in a Computer-Supported Collaborative Environment. Acta Universitatis Lappeenrantaensis.
* Andres, H., & Lander, G. C. (2016). [What’s the Key to Unlocking the Proteasome’s Gate?](http://www.cell.com/structure/abstract/S0969-2126(16)30353-7). Structure, 24(12), 2037-2038.
* Castro, V. F. D., Castro, V. F. D., Frazzon, E. M., & Frazzon, E. M. (2017). Benchmarking of best practices: an overview of the academic literature. Benchmarking: An International Journal, 24(3), 750-774.
* Hajikhani, A. (2017). [Emergence and dissemination of ecosystem concept in innovation studies: A systematic literature review study](https://scholarspace.manoa.hawaii.edu/handle/10125/41796). In Proceedings of the 50th Hawaii International Conference on System Sciences.

### Systematic Mapping Studies
A [systematic mapping study](http://ewic.bcs.org/content/ConWebDoc/19543) (SMS) is a secondary study that aims at classification and thematic analysis of earlier research. The SMS is more general in search terms and aims at classifying and structuring the field of research, while the target of systematic literature review is to summarise and evaluate the research results. According to [Kitchenham and Charters](http://www.elsevier.com/__data/promis_misc/525444systematicreviewsguide.pdf) performing a SMS can be especially suitable if few literature reviews have been done on the topic and there is a need to get a general overview of the field of interest. Both kinds of studies can be used to identify research gaps in the current state of research.

## How to Use

These scripts can be used to complete an exploratory literature review using data downloaded from Web of Knowledge.

### Manually

You can download, install and use our scripts directly. See steps below.

1. Go to Web of Knowledge [website](http://webofknowledge.com/) and select the Web of Science Core Collection from the dropdown menu.
2. Search for literature.
3. Download data. Select Save to Other File Formats from the dropdown menu, enter the range of records (max 500 records for one download), and download Full Record and Cited References. File format should be Tab-delimited (Win) or Tab-delimited (Mac). If you need more than 500 records, repeat the download.
4. Put the downloaded files into the input folder.
5. Open exploration.Rmd with RStudio and press Knit HTML -button. The script will combine the downloaded data into a single file, process it and create visualizations. The results are saved as a HTML-file exploration.html.

See detailed instructions instructions with screenshots for manual processing steps and installation at https://sites.google.com/site/bibliometricdatavisualization/instructions

### Using the Online Analysis Server

_Alternatively_ you can upload files to [our online analysis server](http://hammer.nailsproject.net/). The service is in early beta testing so we appreciate reporting of issues to the [project issues page](https://github.com/aknutas/nails/issues) or as a private Twitter message to [@aknutas](https://twitter.com/aknutas). You can follow the steps below or view a brief [video tutorial](https://youtu.be/I1bRXQs_zMk?list=PLJiFJenPKrLOpdu7E1gEhVEAWF7CLQs_2) on how to get started.

1. Go to Web of Knowledge [website](http://webofknowledge.com/) and select the Web of Science Core Collection from the dropdown menu.
2. Search for literature.
3. Download data. Select Save to Other File Formats from the dropdown menu, enter the range of records (max 500 records for one download), and download Full Record and Cited References. File format should be Tab-delimited (Win) or Tab-delimited (Mac). If you need more than 500 records, repeat the download.
4. Compress the resulting files into a single ZIP archive and upload them to the online analysis server at [hammer.nailsproject.net](http://hammer.nailsproject.net/).
5. Download the results from the web page after the server has processed through the queue.

The script also creates node and edge tables for author and citation networks that can be loaded to Gephi for further exploration.

## We are open source and free software

This program is [free software](https://www.gnu.org/philosophy/free-sw.html): you can redistribute it and/or modify it under the terms of the [GNU General Public License](https://www.gnu.org/licenses/quick-guide-gplv3.html) as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. See LICENSE file for more information.

What does it mean? We are free as in freedom. You may run the software as you wish, for any purpose; you are free to study how the program works, and change it as you wish; you are free to redistribute copies; and you are free to distribute copies of modified versions to others. You may not distribute this software in a non-free manner or add additional restrictions. The only limitations are that you have to follow the free software license, retain the original copyright notices and acknowledgement texts in the program output (section 7b). See links above for more information. If you edit and improve the software, we would love to hear back from you.