{\rtf1\ansi\ansicpg1252\cocoartf1671\cocoasubrtf600
{\fonttbl\f0\fmodern\fcharset0 Courier;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
\margl1440\margr1440\vieww28600\viewh15760\viewkind0
\deftab720
\pard\pardeftab720\sl280\partightenfactor0

\f0\fs24 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 ### A Gaijin\'92s Guide to the Tokyo Train System\
\
![](https://cdn-images-1.medium.com/max/1600/1*xHUN1AVM0ejObXBygvCr9g.jpeg)\
<span class="figcaption_hack">Every day, millions of Japanese use public trains to commute in and around\
Tokyo. With the 2020 Olympics right around the corner, this number is expected\
to increase significantly with the sudden influx of millions of international\
spectators. What can data about Tokyo\'92s public transportation tell us about the\
world\'92s most efficient and complex system? And can we find ways to improve the\
system such that it can operate just as efficiently at much higher capacities?</span>\
\
The Tokyo train system is a logistical marvel to behold. With a population of\
roughly 14 million, coupled with being a bustling international business hub, a\
destination for many young Japanese workers, and the site of the 2020 Olympics,\
the city of [Tokyo](https://en.wikipedia.org/wiki/Tokyo) rarely sleeps. With so\
many people trying to move about the city, a highly efficient public\
transportation system is paramount. And Tokyo has created, arguably, the world\'92s\
best (and most extensive). With rail as the primary means of transportation,\
Tokyo has developed a vast system, consisting of interconnected networks of\
separately owned and operated rail lines and cars, capable of [moving roughly 20\
million passengers\
daily](https://en.wikipedia.org/wiki/Transport_in_Greater_Tokyo#Rail).\
\
With such staggeringly large numbers, I thought it would be interesting to\
analyze one of Tokyo\'92s most popular operators, the Tobu Railway. Data was\
obtained through the [Open Data Challenge for Public Transportation in\
Tokyo](https://tokyochallenge.odpt.org/en/index.html) API, and the full extent\
of the analysis for this post can be found at my\
[GitHub](https://github.com/Nburkhal/Tokyo-Train-Data) page. Though the data\
analyzed is only a small fraction of the overall operation, it does shed some\
light into how truly massive the rail industry is in Japan, as well as into how\
we foreigners can more effectively use the trains to our tourist advantage.\
\
*****\
\
#### Train Volume\
\
Initially, the data was cleaned in order to show how many trains move about the\
Tobu lines throughout the day. It\'92s important to remember that not all trains\
are created equal, so the type of train was added as an extra dimension in the\
analysis. The graph below illustrates the millions of trains Tobu Railway runs\
daily, with emphasis not only on the total number, but also on the volumes of\
*types* of trains.\
\
![](https://cdn-images-1.medium.com/max/1600/1*43IRTEJ3ZjvqTl_3sobraQ.png)\
\
What\'92s telling about this chart is that the total number of trains is at its\
daily highs between 7-9 A.M. and 5-7 P.M. This makes sense because those windows\
are during morning and evening rush, when millions of Japanese salarymen and\
women are commuting to and from their workplaces. Additionally, the Semi-Express\
trains only run through the morning rush, and don\'92t start up again until right\
before evening rush. This signifies that their purpose is to help facilitate the\
sudden influx of people into the stations around Tokyo during these peak hours.\
\
The 8 to 10 P.M. spike is also interesting because it highlights a Japanese\
cultural phenomenon. Japanese workers are expected to leave *after* their\
bosses, and once they leave the office, co-workers are expected get together for\
drinks and dinner. The typical Japanese salaryman typically doesn\'92t get home\
until after 10 P.M. (there is a lot of speculation on whether the Japanese work\
culture has any correlation with the country\'92s declining birth rate, but that\'92s\
a discussion for another time).\
\
The above graph also shows that 3 types of trains make up the bulk of daily\
transportation: Local, Express, and Semi-Express. Percentage-wise, these 3\
trains can be broken down as follows:\
\
![](https://cdn-images-1.medium.com/max/1600/1*jY8DLyn1Rxv6pTty3o62Yw.png)\
\
Here, we can clearly see that local and express trains handle roughly 85% of all\
traffic throughout the day, while the semi-express trains are utilized primarily\
for the rush hours. As a foreigner, if you\'92re trying to get around the city,\
your best bet will be to take a local or express train.\
\
*****\
\
Another point of interest is the variance between inbound and outbound trains.\
While there are only 2 ways a train can move about Tokyo (in or out), there is\
probably a relationship between the time of day and the direction the train is\
moving. The number of inbound and outbound trains was plotted by time of day to\
produce the following visual:\
\
![](https://cdn-images-1.medium.com/max/1600/1*H9y18aO2QiByIU1UBbIlTg.png)\
\
Again, we see peaks in the graph at 7\'969A.M. and 5\'967 P.M. However, if you look\
closely, you can see that there are slightly more inbound trains during the\
morning rush than outbound trains. The opposite is true for the evening rush.\
This is actually highly intuitive, since most people come into Tokyo from\
elsewhere for work, then leave once work is finished. The spike from 8\'9610 P.M.\
also illustrates aforementioned cultural point. However, this influx is also\
partially due to young adults coming into the city to enjoy the Tokyo nightlife.\
\
Percentage-wise, the above graph can be represented as follows:\
\
![](https://cdn-images-1.medium.com/max/1600/1*ftIZiEQFICfaxaEd9hixKQ.png)\
\
What makes this graph interesting is that it clarifies the fact that that more\
trains are inbound throughout the day than outbound, for the reasons mentioned\
above.\
\
*****\
\
#### Station Volume\
\
Now that an idea of train volume is established, the next logical step is to see\
where exactly these trains are going. The Tobu Railway connects 158 stations;\
however, only those that received 20,000 or more inbound trains were included in\
the analysis. This number was chosen as a threshold because the amounts of\
stations that received less varied so much that we would lose insight into which\
stations were the busiest (as the graph would become too cluttered).\
\
![](https://cdn-images-1.medium.com/max/1600/1*30szjnMX1wS_GJ3dRDFxMA.png)\
\
As we can clearly see, the Tobu Zoo Station is by far the busiest in the\
network. However, this does not mean that all the passengers are really excited\
about seeing exotic animals. In fact, the reason for this discrepancy is that\
Tobu Zoo is actually the last stop on the Tobu Railway route. This means that\
Tobu Station is used to transfer to other railways, and essentially acts as a\
hub to get into and out of Tokyo via the Tobu line.\
\
*****\
\
#### Line Volume\
\
The final analysis was to determine which rail lines were the busiest. Inbound\
and outbound trains were calculated based on specific Tobu Railway lines.\
\
![](https://cdn-images-1.medium.com/max/1600/1*rC_ZjouFJ9JyfWKeRLuBAg.png)\
\
This graph illustrates that the Kosuge, Horikiri, and Tokyo Skytree lines make\
up the vast majority of the Tobu Railway system. All the other lines are\
offshoots to more specific locations within Tokyo. As a tourist, your best bet\
to get anywhere will be to use one of these three lines.\
\
*****\
\
#### Conclusion\
\
The Tokyo public rail operation is unfathomably massive and complex. In this\
post, I only outlined one specific railway. In reality, there are 29 other\
operators operating a total of 108 separate lines connecting a total of 882 rail\
stations within Tokyo. Due to the network\'92s design, it is practically impossible\
to get a hold of all of the city\'92s train data for analysis purposes; however, we\
can still glean some important insights from even a small fraction of the\
overall picture. As tourists, we should expect extremely crowded stations during\
the morning and evening rush hours. We should also expect that our travel will\
be less crowded if we decide to come into Tokyo during the evenings as opposed\
to leaving (the opposite is true for the morning). Additionally, the Pareto Rule\
holds true for rail lines \'97 most of your transportation can be accomplished on a\
small fraction of the operator\'92s lines. Finally, the last stop on a train\'92s\
route is usually the busiest, as many people are transferring lines to move\
about the country.\
}