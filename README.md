## MSc. Thesis: Stadia and Sporting Events in London, Use of GPS Data to analyse Spectator Behaviour

### GitHub Folder Overview 
  1. **BigQuery** - Folder with BigQuery scripts to access the data for further analysis. 
  2. **Event Categories** - Folder with the graphs results for each different sporting events. 
  3. **Shapefiles** - Geographic location data file for analysis
  4. **iPython Colab** - Colab Notebook with code for temporal, spatial and statistical analysis. 
  5. **Images Thesis** - Visualisation use in the thesis presentaiton. (Non geographic images). 

### Project Background
Sporting events play a major role in cities, contributing to community engagement and international appeal. The stadia have evolved into multi-facility areas, incorporating shopping centres, restaurants, team’s museum, thus leading to changes in event consumption. Investigating the characteristics of event attendees is a continuing concern for event planners and government officials. On the one hand, it allows them to mitigate negative effects such as traffic congestion and urban disorder, and, on the other, help them to provide tailored services; satisfying usual customers and potentially attracting new ones. The development of smart devices and GPS technology has created new opportunities to undertake an in-depth analysis of spectators’ characteristics.

### Data and Methods
This study aims to explore whether various sports events and stadia create changes in spectator behaviour. The dataset consisted of anonymised GPS data from September 2017 to January 2018. The data covered 35 sports events (2018 FIFA World Cup Qualification, UEFA Champions League, English Premier League (EPL), NFL, and rugby games) across 4 stadia in London (London Stadium, Twickenham, Vicarage Road, and Wembley). The clean dataset included 89,206 individuals for which the user_id, timestamp, longitude, and latitude coordinates were available. After extracting sports events spectators considering their presence in the event stadium at day and time of an event, the dataset was left with 30,079 individuals. 

Temporal, spatial and demographic factors were chosen to analyse the spectator behaviour. First, the arrival, departure, and dwell time of the spectators in the event area was determined. The event area was drawn manually, representing a polygon encompassing the stadium, its surroundings, and possibly closest underground stations. Second, the home location and the travel distance of the spectators were inferred from the GPS dataset. The criteria to consider spectator’s location as spectators’ home were: the recorded time, cluster diameter, and number of days of the spectators’ GPS points. The travel distance was computed using the Google Distance Matrix API. Finally, the spectators’ demographic profile was defined using ACORN segmentation. Each spectators’ home was matched to its corresponding UK postcode, thus assigned into one of the 6 ACORN category or 18 ACORN group.

### Key Findings
This study highlights differences in spectator behaviour according to venue and type of events.
<p align="center">
<img src="/Event%20Categories/District_Selection/Premier%20League%20-%20wembley%20stadium.png" width="250" style="top: -10px"/><img src="/Event%20Categories/District_Selection/Premier%20League%20-%20vicarage%20road.png" width="250"/><img src="/Event%20Categories/District_Selection/Premier%20League%20-%20london%20stadium.png" width="250"/>
</p>
<p align="center">
<em>Figure 1: District Catchment area for EPL games at Wembley, Vicarage Road and London Stadium.</em>
</p>

Events from second importance such as EPL games show a smaller catchment area than renowned events such as NFL, UEFA or rugby games. Similarly, stadia with large facilities such as Wembley attract spectators from broader geography than modest stadia such as Vicarage Road. Moreover, one-off events like NFL games influence considerably the temporal behaviour of the spectators. In contrast to EPL games, for which spectators temporal profile displays an obvious trend, with arrival and departure peaks, NFL spectators temporal profile shows a steady pattern of spectators’ incoming and outgoing, occurring over a wider period of time.

### Value of the Research 
This research enhanced the understanding of sports spectator behaviour. The findings may benefit event managers to target more precisely their customers using the spectators’ home location as well as spectators’ demographic characteristics. Moreover, the temporal analyses may help transport planners to better manage spectators flows. The analyses carried in this work could be employed to build predictive models to assess the likelihood of residents from UK postcodes to attend specific sports events or forecast the temporal behaviour of a spectator.
