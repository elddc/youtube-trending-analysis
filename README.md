# Youtube Video Analysis and Classification

This project analyzes trending YouTube videos from August 2020 to present. It explores the attributes of trending videos, such popular channels, categories, and keywords. It also trains a stochastic gradient descent model to classify videos by category, using tokens extracted from video titles and tags by NLTK.

[Data Source](https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset)

## Results

Number of unique videos indexed: 38747

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
      <th>212991</th>
      <td>Jawan |Official Hindi Prevue |Shah Rukh Khan |...</td>
      <td>Red Chillies Entertainment</td>
      <td>Entertainment</td>
      <td>2023-07-10 04:58:09</td>
      <td>SRK|Shah rukh khan|shahruh khan|Srk movies|red...</td>
      <td>51798724</td>
    </tr>
    <tr>
      <th>213788</th>
      <td>정국 (Jung Kook) 'Seven (feat. Latto)' Official MV</td>
      <td>HYBE LABELS</td>
      <td>Music</td>
      <td>2023-07-14 04:00:00</td>
      <td>HYBE|HYBE LABELS|하이브|하이브레이블즈|정국|Jung Kook|Seven</td>
      <td>41185831</td>
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
      <th>212588</th>
      <td>Train Vs Giant Pit</td>
      <td>MrBeast</td>
      <td>Entertainment</td>
      <td>2023-07-08 16:00:00</td>
      <td>[None]</td>
      <td>33142241</td>
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
      <td>65</td>
      <td>1291342767</td>
    </tr>
    <tr>
      <th>NBA</th>
      <td>Sports</td>
      <td>367</td>
      <td>719057959</td>
    </tr>
    <tr>
      <th>HYBE LABELS</th>
      <td>Music</td>
      <td>67</td>
      <td>703937472</td>
    </tr>
    <tr>
      <th>BLACKPINK</th>
      <td>Music</td>
      <td>57</td>
      <td>689071265</td>
    </tr>
    <tr>
      <th>SMTOWN</th>
      <td>Music</td>
      <td>74</td>
      <td>601840367</td>
    </tr>
    <tr>
      <th>NFL</th>
      <td>Sports</td>
      <td>329</td>
      <td>529529265</td>
    </tr>
    <tr>
      <th>JYP Entertainment</th>
      <td>Music</td>
      <td>75</td>
      <td>501748170</td>
    </tr>
    <tr>
      <th>BANGTANTV</th>
      <td>Music</td>
      <td>74</td>
      <td>492688501</td>
    </tr>
    <tr>
      <th>MrBeast Gaming</th>
      <td>Gaming</td>
      <td>77</td>
      <td>477439867</td>
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
      <td>7609</td>
      <td>11319529027</td>
    </tr>
    <tr>
      <th>Music</th>
      <td>JYP Entertainment</td>
      <td>6126</td>
      <td>10805752685</td>
    </tr>
    <tr>
      <th>Gaming</th>
      <td>SSundee</td>
      <td>7706</td>
      <td>7705949654</td>
    </tr>
    <tr>
      <th>Sports</th>
      <td>NBA</td>
      <td>4850</td>
      <td>5430000082</td>
    </tr>
    <tr>
      <th>People &amp; Blogs</th>
      <td>Ryland vlogs</td>
      <td>3399</td>
      <td>3274057443</td>
    </tr>
    <tr>
      <th>Film &amp; Animation</th>
      <td>The Film Theorists</td>
      <td>1474</td>
      <td>2038739612</td>
    </tr>
    <tr>
      <th>Comedy</th>
      <td>The Try Guys</td>
      <td>1926</td>
      <td>1759602894</td>
    </tr>
    <tr>
      <th>Science &amp; Technology</th>
      <td>SpaceX</td>
      <td>1160</td>
      <td>1638284204</td>
    </tr>
    <tr>
      <th>News &amp; Politics</th>
      <td>TODAY</td>
      <td>1423</td>
      <td>1379830580</td>
    </tr>
    <tr>
      <th>Education</th>
      <td>Veritasium</td>
      <td>909</td>
      <td>845022489</td>
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
      <td>34830</td>
      <td>33580390908</td>
      <td>9.641226e+05</td>
    </tr>
    <tr>
      <th>video</th>
      <td>video</td>
      <td>24278</td>
      <td>34699189288</td>
      <td>1.429244e+06</td>
    </tr>
    <tr>
      <th>game</th>
      <td>game</td>
      <td>22004</td>
      <td>26083874834</td>
      <td>1.185415e+06</td>
    </tr>
    <tr>
      <th>new</th>
      <td>new</td>
      <td>19028</td>
      <td>22807741340</td>
      <td>1.198641e+06</td>
    </tr>
    <tr>
      <th>v</th>
      <td>v</td>
      <td>17784</td>
      <td>23170427768</td>
      <td>1.302881e+06</td>
    </tr>
    <tr>
      <th>highlight</th>
      <td>highlight</td>
      <td>17544</td>
      <td>20988444796</td>
      <td>1.196332e+06</td>
    </tr>
    <tr>
      <th>official</th>
      <td>official</td>
      <td>14652</td>
      <td>23290492236</td>
      <td>1.589578e+06</td>
    </tr>
    <tr>
      <th>music</th>
      <td>music</td>
      <td>13432</td>
      <td>19947386876</td>
      <td>1.485065e+06</td>
    </tr>
    <tr>
      <th>none</th>
      <td>none</td>
      <td>12852</td>
      <td>18813573170</td>
      <td>1.463863e+06</td>
    </tr>
    <tr>
      <th>fortnite</th>
      <td>fortnite</td>
      <td>12404</td>
      <td>9355179560</td>
      <td>7.542067e+05</td>
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

 
