---
title: Click Depth - Why and How it matters for a Website’s pagination and SEO
categories:
  - SEO
featured-image: pagination.webp
slug: click-depth-website-pagination-seo
excerpt: A website's pagination is good from a human’s point of view; however, it’s bad for a search engine crawler if not optimized well. We all see pagination links as clickable numbers; buttons like Next/ previous are often used to define a website’s pagination. However, there’s more to pagination than to view it as a source of navigation. In this article, I will walk you through a piece of actionable advice on how to approach a website’s SEO with pagination.
redirect_from: "/seo/2019/11/10/click-depth-website-pagination-seo/"
author: Rakshit Soral

---
Website pagination is good from a human’s point of view; however, it’s bad for a search engine crawler if not optimized well.



We all see pagination links as clickable numbers; buttons like Next/ previous are often used to define a website’s pagination. However, there’s more to pagination than to view it as a source of navigation. 



In this article, I will walk you through a piece of actionable advice on how to approach a website’s SEO with pagination. Continue reading on and you will find out the relation between Pagination, Click depth and Crawl Budget.



Let’s dive in!



## The Anatomy of a 300 Pages Website and SEO performance



Imagine having a site with pagination from 1…...300. For the purpose of this example, let’s assume they are blog posts with unique content. Here page number 1 is the Home page of the website and 300 is the last page of the website. 



Now assume that the site consists of pagination where these pages are connected to a simple “next page” link at the bottom of each blog post. 



From a human's point of view, the pagination scheme is simple: you click the “next page” link and it takes you to the blog post number 2. You click on the “next page” one more time, it takes you to the number 3. To visit each and every page (say 300 times), you need to keep clicking on “next page” until you reach the page you want to visit. That’s a holy grail of website pagination. Isn’t it?



From the crawler’s point of view, however, the site looks like this:
![Simplest pagination](/images/300 Pagination.jpg)<br>





The image above represents a visual representation of a discovery path that an SE crawler has to follow to crawl the whole 300-page website. Note that, for each page, the “next page” link works like navigation to the consecutive page. 



The tail shown in the diagram is a “tunnel” which represents a long connected sequence of pages that the SE crawler has to crawl at a time. 



## The Importance of Click Depth



The term ‘Click Depth” describes the number of clicks needed from the homepage to navigate on the other page. 



For instance: the page clicked from your homepage has a click-depth of one. But why do I introduced this term just after the above diagram? Let’s jump in!



In a recent <a href="https://www.searchenginejournal.com/google-click-depth-matters-seo-url-structure/256779/#close" target="_blank"> Google Webmaster Central hangout chat</a>, Google’s John Muller revealed the concept of Click depth and justified that it is more important for SEO as compared to URL structure.



In the words of Muller,



<div class="mb-wrap mb-style-2"><blockquote><p>“What does matter for us ... is how easy it is to actually find the content. So especially if your homepage is generally the strongest page on your website, and from the homepage, it takes multiple clicks to actually get to one of these stores, then that makes it a lot harder for us to understand that these stores are actually pretty important."<br>



“On the other hand, if it’s one click from the home page to one of these stores then that tells us that these stores are probably pretty relevant, and that probably we should be giving them a little bit of weight in the search results as well. So it’s more a matter of how many links you have to click through to actually get to that content rather than what the URL structure itself looks like.”</p><span>John Muller</span></blockquote></div>

 



In essence: If a page needs more than 3 clicks to be reached, it’s performance will be considered as poorly to search engines. Hence, the pages that are deeper in your website silo’s will have issues to crawl as compared to the page of click depth one or two. 



If the stats are to be believed, deep pages have a lower page rank because search engines are less likely to find them. Hence, crawling issues will be there. These pages are less likely to perform and rank as compared to the pages that are easily find from the home page. 



In our example of the 300 pages website, the last page will have a click-depth of 300. The key takeaway from this kind of website pagination is that the traditional form of “next” and “previous” type of pagination is simply inefficient. Neither it is good for SEO, nor user experience. 



If I were to make a list of problems that “Next” and “Previous” kind of pagination has, then here would be my key points:

<ul class="round">

<li>When a site’s content gets buried deep in the form of links, it sends a poor message to the search engines that the content is not important for users. Hence, bad SEO. </li>

<li>Even worse, if any of the links among “next” and “previous” returns an error, crawlers will not crawl the pages that are deep inside the pagination.</li>

<li>Website visitors won’t click up to the 300th page or even lesser than that. That’s bad user experience. </li>

</ul>



So, how can the pagination problem in the above example be solved?



## Enters the Midpoint link pagination scheme



The midpoint link pagination scheme is best for sites having a large number of pages. Here, pagination for the homepage looks like this:

![simplest mid point pagination](/images/simplest mid point pagination.jpg)

In the above image, 201 is the midpoint of the pagination and it lowers down the click depth from 300 to only few clicks. What’s more, this scheme makes it possible for a crawler to navigate from any page to any other page in just few steps. 

Here’s the crawl chart for the same:

 ![crawl chart for midpoint pagination](/images/crawl chart for midpoint pagination1.jpg)



This lead us to an incredible level of crawlability improvement as compared to the previous “next” and “previous” pagination scheme. 



<h2 class="note">Conclusion</h2>



Click depth (also referred to as Page depth sometimes) should be a key consideration while designing pagination for a website with a large structure. With the right approach, SEO can get the most out of Googlebot’s crawl budget, thereby improving the visibility of the site’s content. 



How’s the pagination of your website look like, let me know in the comment section.
