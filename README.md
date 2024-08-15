# thesis


### Topics

There's two major line of enquiry for the thesis. The first one is the centre's current research area, which is short-term conventional ML-based weather modelling. The second is my original idea, which is applications of long-term climate modelling combined with conventional geospatial methods to identify areas of urban and rural insight.

&nbsp;  

### climateModelling

which is really more like weather modelling; This is most of the work we've done with the centre over the summer.
 
### Data

 - IMD has 1x1 temperature from 1951 to 2024 - which we've downloaded as ``heat_main``.
 - IMD has 2.5x2.5 temperature from June 2015 to 2024, which is about 9 years, which we've downloaded as ``heat_rt``. Is 9 years enough to draw meaningful inferences? It definitely isn't for climate, but maybe for weather?
 - [ERA-5 hourly pressure data](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-pressure-levels?tab=form)
 - [Bhuvan DEM](https://bhuvan-app3.nrsc.gov.in/data/download/index.php?c=s&s=C1&p=cdv2&g)
 - [Heat and moisture based heatwave maps](https://bhuvan-app1.nrsc.gov.in/heatwave/)

### Lit Review

 - [Lit review presentation](https://www.canva.com/design/DAGKtv2ri6c/f_HtVsEyY5WYIoyXIgBkZg/edit)
 - [Lit review (Sapta)]()
 - [Lit review (Divij)](https://github.com/kkkarnav/thesis/blob/main/Paper_Presentations%20(Divij).pdf)
 - [Work Report (Divij)](https://github.com/kkkarnav/thesis/blob/main/Weather%20Modelling%20Report%20(Divij).pdf)

 - Data:
     - [IMD Lib] [IMDLIB: An open-source library for retrieval, processing and spatiotemporal exploratory assessments of gridded meteorological observation datasets over India](https://www.sciencedirect.com/science/article/abs/pii/S1364815223002554)
     - [Global weather station dataset][WEATHER-5K: A Large-scale Global Station Weather Dataset Towards Comprehensive Time-series Forecasting Benchmark](https://github.com/taohan10200/WEATHER-5K?tab=readme-ov-file)

 - Methods:
     - [Statistical overview] [Review of trend detection methods and their application to detect temperature changes in India - P. Sonali, D. Nagesh Kumar (2012)](https://www.sciencedirect.com/science/article/abs/pii/S0022169412009341?via%3Dihub)
     - [(tmax+tmin)/2 isn't a good estimate] [On the min–max estimation of mean daily
temperatures](https://bpb-us-w2.wpmucdn.com/sites.uwm.edu/dist/f/330/files/2019/10/Clim.-Dyn.-min-max.pdf)
     - [Statistical trends in IMD data] [Spatial and Temporal Trends in High Resolution Gridded Temperature Data over India](https://link.springer.com/article/10.1007/s13143-019-00120-1)
     - [Normal distribution conversion of temperature] [On the statistical distribution of temperature and the classification of extreme events considering season and climate change—an application in Switzerland](https://link.springer.com/article/10.1007/s00704-023-04530-0)
     - [Indian rainfall analysis][Characteristics of southwest summer monsoon rainfall events over East India](https://www.researchgate.net/publication/342165818_Characteristics_of_southwest_summer_monsoon_rainfall_events_over_East_India)
     - [Downscaling weather predictions with AI] [Emerging AI-based weather prediction models as downscaling tools](https://arxiv.org/pdf/2406.17977)
 
 - Models:
     - [Georgia NN weather prediction] [Artificial neural networks for automated year-round temperature prediction](https://sci-hub.se/http://dx.doi.org/10.1016/j.compag.2009.04.003)
 - Related Models:
     - [Climate induced disaster prediction] [Impact Analysis of Climate Change on Floods in an Indian Region Using Machine Learning](https://link.springer.com/chapter/10.1007/978-3-031-44198-1_31)
     - [Physical climate forecast] [Improved Surface Temperature Prediction for the Coming Decade from a Global Climate Model - Smith (2007)](https://sci-hub.se/https://doi.org/10.1126/science.1139540)
    

### Statistics & Preprocessing

 - Dickey-Fuller & KPSS
 - Seasonal & STL Decomposition

### Models

 - Autoformer?
 - Linear Regression - terrible results
 - STL Forecast - failed to forecast seasonal trend
 - [tsai - Set of timeseries models](https://github.com/timeseriesAI/tsai)
 - [Google NeuralGCM](https://github.com/google-research/neuralgcm)
 - [Google GraphCast](https://deepmind.google/discover/blog/graphcast-ai-model-for-faster-and-more-accurate-global-weather-forecasting/)
 - [SHIELD: USGov atmospheric model](https://shield.gfdl.noaa.gov/shield-in-a-box/)
 - [Pritvhi: NASA foundational model](https://www.karmactive.com/nasa-and-ibms-prithvi-model-a-12x-boost-in-climate-forecast-accuracy/)

### Benchmarks

 - [WeatherBench 2](https://blog.research.google/2023/08/weatherbench-2-benchmark-for-next.html)
 - 

### Ideas

 - Markov chains for weather prediction
 - Satellite images?
 - Look for satellite image inference literature

### People

 - [Thierry Roncalli, Evry Paris Saclay](https://research-center.amundi.com/thierry-roncalli)

### To Do

 - Replicate the experiments
 - Figure out reanalysis
 - Use satellite image data products
 - Explore ISRO data

&nbsp;  

### pricingLand

which is not as clearly defined; This is most of the work I've been interested in doing geospatially.
 
### Data

 - Each state has a BhuNaksha instance which has point-accurate polyons of each plot of land. The [availability](https://bhunaksha.nic.in/bhunaksha/implementationstatus.jsp) is: Himachal, Uttar Pradesh, Rajasthan, Maharashtra, Bihar, Odisha, Jharkhand, Chattisgarh, Andhra, Goa, Kerala. The main missing states are Uttarakhand, Gujarat (BhuLekh solution), WB, Telangana, Karnataka, and Tamil Nadu.

### Lit Review

 - Data:

 - Methods:
     - [Survey of climate risk pricing] [Pricing of climate risks in financial markets: a summary of the literature](https://www.bis.org/publ/bppdf/bispap130.pdf)
     - [Survey of climate risk-adjusted portfolio construction] [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3999971](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3999971)
     - [Real estate climate risk factor] [https://www.msci.com/www/blog-posts/measuring-climate-risk-in-real/01973063966](https://www.msci.com/www/blog-posts/measuring-climate-risk-in-real/01973063966)
 
 - Models:
     

### Statistics & Preprocessing

 - 

### Models

 - 

### Ideas

 - Climate risk pricing model, where loss function is modified by some sort of climate risk index
 - Would it be possible to get circle rates for every state from government websites?
 - 99acres is scrapeable, for urban data?

### People

 - [Anupam Sobti, Plaksha](https://anupamsobti.github.io/)

### To Do

 - 
