# Youtube Video Analysis and Classification

This project analyzes trending YouTube videos from August 2020 to present. It explores the attributes of trending videos, such popular channels, categories, and keywords. It also trains a linear SVC model to classify videos by category, using tokens extracted from video titles and tags by NLTK.

[Data Source](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset)

## Results

Number of unique videos indexed: 38423

### Top Videos of All Time

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>channel_title</th>
      <th>category</th>
      <th>published_at</th>
      <th>tags</th>
      <th>view_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>212189</th>
      <td>Salaar Teaser | Prabhas, Prashanth Neel, Prith...</td>
      <td>Hombale Films</td>
      <td>Entertainment</td>
      <td>2023-07-05 23:41:10</td>
      <td>salaar update|salaar teaser|salaar|salaar teas...</td>
      <td>91463891</td>
    </tr>
    <tr>
      <th>80193</th>
      <td>LISA - 'LALISA' M/V</td>
      <td>BLACKPINK</td>
      <td>Music</td>
      <td>2021-09-10 04:00:13</td>
      <td>YG Entertainment|YG|와이지|K-pop|BLACKPINK|블랙핑크|블...</td>
      <td>85890366</td>
    </tr>
    <tr>
      <th>100194</th>
      <td>Crazy #alluarjun #painting  #shorts #viral #tr...</td>
      <td>Dr.Harrsha Artist</td>
      <td>Film &amp; Animation</td>
      <td>2021-12-08 13:16:02</td>
      <td>[None]</td>
      <td>79283769</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Cardi B - WAP feat. Megan Thee Stallion [Offic...</td>
      <td>Cardi B</td>
      <td>Music</td>
      <td>2020-08-07 04:00:10</td>
      <td>Cardi B|Cardi|Atlantic Records|rap|hip hop|tra...</td>
      <td>76805026</td>
    </tr>
    <tr>
      <th>114216</th>
      <td>Hey man, we are Italian 🇮🇹😅🤷🏼‍♀️#shorts #funny...</td>
      <td>Jessi &amp; Sean</td>
      <td>People &amp; Blogs</td>
      <td>2022-02-20 20:42:28</td>
      <td>[None]</td>
      <td>71401624</td>
    </tr>
  </tbody>
</table>
</div>


### Top Videos This Month

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>channel_title</th>
      <th>category</th>
      <th>published_at</th>
      <th>tags</th>
      <th>view_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>212189</th>
      <td>Salaar Teaser | Prabhas, Prashanth Neel, Prith...</td>
      <td>Hombale Films</td>
      <td>Entertainment</td>
      <td>2023-07-05 23:41:10</td>
      <td>salaar update|salaar teaser|salaar|salaar teas...</td>
      <td>91463891</td>
    </tr>
    <tr>
      <th>207388</th>
      <td>$1 vs $1,000,000,000 Yacht!</td>
      <td>MrBeast</td>
      <td>Entertainment</td>
      <td>2023-06-10 16:00:00</td>
      <td>[None]</td>
      <td>39951228</td>
    </tr>
    <tr>
      <th>211790</th>
      <td>#RockyAurRaniKiiPremKahaani - OFFICIAL TRAILER...</td>
      <td>Dharma Productions</td>
      <td>Film &amp; Animation</td>
      <td>2023-07-04 06:30:09</td>
      <td>rocky aur rani|ranveer singh|ranveer singh new...</td>
      <td>36842906</td>
    </tr>
    <tr>
      <th>210464</th>
      <td>LEO - Naa Ready Lyric Video | Thalapathy Vijay...</td>
      <td>Sony Music South</td>
      <td>Music</td>
      <td>2023-06-22 13:00:04</td>
      <td>Sony Music South|Sony Music|Latest Song|Tamil ...</td>
      <td>29476135</td>
    </tr>
    <tr>
      <th>210995</th>
      <td>Tum Kya Mile - Rocky Aur Rani Kii Prem Kahaani...</td>
      <td>Saregama Music</td>
      <td>Music</td>
      <td>2023-06-28 06:30:08</td>
      <td>Tum Kya Mile|tu kya mile|rocky aur ranii ki pr...</td>
      <td>28188098</td>
    </tr>
  </tbody>
</table>
</div>


### Top 10 Most Popular Channels

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>category</th>
      <th>video_count</th>
      <th>total_views</th>
    </tr>
    <tr>
      <th>channel_title</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>MrBeast</th>
      <td>Entertainment</td>
      <td>64</td>
      <td>1258200526</td>
    </tr>
    <tr>
      <th>NBA</th>
      <td>Sports</td>
      <td>365</td>
      <td>716335767</td>
    </tr>
    <tr>
      <th>BLACKPINK</th>
      <td>Music</td>
      <td>57</td>
      <td>689071265</td>
    </tr>
    <tr>
      <th>HYBE LABELS</th>
      <td>Music</td>
      <td>63</td>
      <td>630171785</td>
    </tr>
    <tr>
      <th>SMTOWN</th>
      <td>Music</td>
      <td>73</td>
      <td>596206850</td>
    </tr>
    <tr>
      <th>NFL</th>
      <td>Sports</td>
      <td>329</td>
      <td>529529265</td>
    </tr>
    <tr>
      <th>BANGTANTV</th>
      <td>Music</td>
      <td>72</td>
      <td>483997142</td>
    </tr>
    <tr>
      <th>JYP Entertainment</th>
      <td>Music</td>
      <td>73</td>
      <td>475306303</td>
    </tr>
    <tr>
      <th>MrBeast Gaming</th>
      <td>Gaming</td>
      <td>76</td>
      <td>464474880</td>
    </tr>
    <tr>
      <th>SSSniperWolf</th>
      <td>Entertainment</td>
      <td>117</td>
      <td>441121235</td>
    </tr>
  </tbody>
</table>
</div>

### Top 10 Most Popular Categories

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>top_channel</th>
      <th>video_count</th>
      <th>total_views</th>
    </tr>
    <tr>
      <th>category</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Entertainment</th>
      <td>SSSniperWolf</td>
      <td>7534</td>
      <td>11110425977</td>
    </tr>
    <tr>
      <th>Music</th>
      <td>JYP Entertainment</td>
      <td>6063</td>
      <td>10581632934</td>
    </tr>
    <tr>
      <th>Gaming</th>
      <td>SSundee</td>
      <td>7643</td>
      <td>7652487573</td>
    </tr>
    <tr>
      <th>Sports</th>
      <td>NBA</td>
      <td>4813</td>
      <td>5397357247</td>
    </tr>
    <tr>
      <th>People &amp; Blogs</th>
      <td>Unspeakable</td>
      <td>3381</td>
      <td>3263650055</td>
    </tr>
    <tr>
      <th>Film &amp; Animation</th>
      <td>The Film Theorists</td>
      <td>1455</td>
      <td>2004977179</td>
    </tr>
    <tr>
      <th>Comedy</th>
      <td>The Try Guys</td>
      <td>1917</td>
      <td>1751954766</td>
    </tr>
    <tr>
      <th>Science &amp; Technology</th>
      <td>SpaceX</td>
      <td>1150</td>
      <td>1630478802</td>
    </tr>
    <tr>
      <th>News &amp; Politics</th>
      <td>TODAY</td>
      <td>1421</td>
      <td>1379421249</td>
    </tr>
    <tr>
      <th>Education</th>
      <td>Veritasium</td>
      <td>900</td>
      <td>836960823</td>
    </tr>
  </tbody>
</table>
</div>

### Top 10 Most Common Keywords

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>token</th>
      <th>video_count</th>
      <th>view_count</th>
      <th>avg_views</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>minecraft</th>
      <td>minecraft</td>
      <td>34508</td>
      <td>33380448882</td>
      <td>9.673249e+05</td>
    </tr>
    <tr>
      <th>video</th>
      <td>video</td>
      <td>24108</td>
      <td>34381882370</td>
      <td>1.426161e+06</td>
    </tr>
    <tr>
      <th>game</th>
      <td>game</td>
      <td>21848</td>
      <td>25972128652</td>
      <td>1.188765e+06</td>
    </tr>
    <tr>
      <th>new</th>
      <td>new</td>
      <td>18894</td>
      <td>22332231952</td>
      <td>1.181975e+06</td>
    </tr>
    <tr>
      <th>v</th>
      <td>v</td>
      <td>17668</td>
      <td>22932122040</td>
      <td>1.297947e+06</td>
    </tr>
    <tr>
      <th>highlight</th>
      <td>highlight</td>
      <td>17456</td>
      <td>20908652800</td>
      <td>1.197792e+06</td>
    </tr>
    <tr>
      <th>official</th>
      <td>official</td>
      <td>14498</td>
      <td>22655730148</td>
      <td>1.562680e+06</td>
    </tr>
    <tr>
      <th>music</th>
      <td>music</td>
      <td>13336</td>
      <td>19848655476</td>
      <td>1.488351e+06</td>
    </tr>
    <tr>
      <th>none</th>
      <td>none</td>
      <td>12756</td>
      <td>18654062734</td>
      <td>1.462376e+06</td>
    </tr>
    <tr>
      <th>fortnite</th>
      <td>fortnite</td>
      <td>12374</td>
      <td>9337444342</td>
      <td>7.546019e+05</td>
    </tr>
  </tbody>
</table>
</div>


### Top Minecraft Videos
The most common keyword was minecraft.

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>channel_title</th>
      <th>category</th>
      <th>published_at</th>
      <th>tags</th>
      <th>view_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>83636</th>
      <td>realistic lava vs water in minecraft</td>
      <td>steveee</td>
      <td>Gaming</td>
      <td>2021-09-27 07:00:10</td>
      <td>minecraft|realistic|physics|water|shaders|mine...</td>
      <td>4264951</td>
    </tr>
    <tr>
      <th>81799</th>
      <td>realistic lava in minecraft</td>
      <td>steveee</td>
      <td>Gaming</td>
      <td>2021-09-18 07:00:30</td>
      <td>minecraft|realistic|physics|water|snapshot|mod...</td>
      <td>3870630</td>
    </tr>
    <tr>
      <th>122015</th>
      <td>when minecraft removed the inventory... (april...</td>
      <td>camman18</td>
      <td>Entertainment</td>
      <td>2022-04-09 15:00:01</td>
      <td>camman18|camman18 minecraft|minecraft|minecraf...</td>
      <td>2885109</td>
    </tr>
    <tr>
      <th>119244</th>
      <td>revisiting old minecraft textures</td>
      <td>camman18</td>
      <td>Entertainment</td>
      <td>2022-03-26 15:00:17</td>
      <td>camman18|camman18 minecraft|minecraft|minecraf...</td>
      <td>2274038</td>
    </tr>
    <tr>
      <th>116391</th>
      <td>what if minecraft didn't have wood...</td>
      <td>camman18</td>
      <td>Entertainment</td>
      <td>2022-03-12 16:00:21</td>
      <td>camman18|camman18 minecraft|minecraft|minecraf...</td>
      <td>2224013</td>
    </tr>
  </tbody>
</table>
</div>

 
