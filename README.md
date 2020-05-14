## Tracking  # of COVID-19 cases in Alameda County California using Statistical Process Control
[Link to Tableau Dashboard](https://public.tableau.com/profile/brenton.hsu5940#!/vizhome/AlamedaCountyControlChartCovid-19Cases/Overview?publish=yes)


## Summary
While watching the news on television, I watch the anchor display a trend graph of daily COVID-19 cases in the county I live in and describe the graph as if every data point signaled a uptick, flattening, or downtick in COVID-19 cases. For example, the anchor would say that the "curve was flattening" after seeing two days of decreasing cases or the anchor would imply COVID-19 cases were getting worst after seeing a spike in the data. However, the anchor scrutinizing every data point of # cases of COVID-19 could be harmful and lead to an over reaction or panic to the viewers. Instead, the data should be looked at holistically and statistically to determine if each new day of # of COVID-19 cases signal any meaning. 

Spikes and random patterns are always naturally appearing in data and are generally common cause variation. An example of common cause variation would be the # of people who shop in a specific grocery store each day. Obviously, the grocery store would expect the # of people to shop in the grocery store to change on a day to day basis, this is the expected common cause variation. On the other hand, a start of a shelter in place order could significantly increase the # of people to shop on that day, this would be a special cause variation, because their was no expectation of this to happen based on historical data. Detecting these special cause variation are important, because they can signal that an event that triggered your data to have an outlier or your data common cause variation could be changing. 

By leveraging control charts, I analyzed the data to determined the common cause variation in the daily # of COVID-19 cases in Alameda County and what daily spikes are special cause variation. As a result, I am able to determine if each new daily data point of # of COVID-19 cases are signaling any potential issues or if Alameda County can expect a change in common cause variation of # of COVID-19 cases. Specifically, Alameda County can currently expect their to be between 3 and 82 COVID-19 cases each day with an average of 43 cases. Any day with the # of cases spiking above 82 signals a special cause and should be analyzed further to see if this was a one time event or if the common cause variation could be changing due to a process change. An example of a process change could be a change in response from Alameda County, such as moving from Phase I to Phase II of shelter in place. This process change would then require for the Control Chart to be recalculated to get an updated view of the expected # of daily COVID-19 cases. On the other spectrum, a downtick below 3 cases in a day signals a special cause variation, which can also be due to a process change or one time event. 

Based on the controls chart, I recommend viewers to not be alarm or panic at any spikes that are below 82 cases. Instead, these spikes are expected common cause variation and the impact of COVID-19 is probably not getting worst. However, if a spike above 82 case is detected than that should be a signal for the viewer to check for any COVID-19 related news to see their is a reason for this spike.  

Below are the Control Charts that are used to detect significant spikes in # of COVID-19 cases in Alameda County. Any date after 5/6 are not included in calculating the control limits, since they were locked to start detecting any significant spikes in cases. Control limits (UCL, LCL) are the calculated values of the expected range of daily # of cases.
![](3_images/dashboard_screenshot.png)


## Future Steps
Moving forward, I am locking the control limits to be able to detect any future special cause events that can be signally a change in the impact of COVID-19. Additionally, a deeper analysis may be done to detect any trends are special cause variation, which can lead to a smaller range of control limits. Also, additional flags can be added to detect special causes besides spikes. For example, special causes can also be trends in the data that are statistically unlikely given the current status of COVID-19, which could be signal in change in COVID-19 impact.


## Appendix 

## Data
The data is downloaded from Alameda County Open Data at this link [acgov link](https://data.acgov.org/datasets/AC-HCSA::alameda-county-covid-19-cases-and-deaths-over-time-1/data)

One major nuance is that the Alameda County total case count needs to add together Berkeley and Alameda County total case counts, since they are consider different local health jurisdiction (LHJ)

## Control Chart
Based on the process of COVID-19daily cases, I use a I-MR Chart, because the data cannot be subgrouped.

## Analysis
Based on the control charts, the majority of the daily COVID-19 cases in Alameda County should fall between 3 and 82 cases daily with an average of 43.
