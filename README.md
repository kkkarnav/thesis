# thesis


### Topics

There's two major line of enquiry for the thesis. The first one is the centre's current research area, which is short-term conventional ML-based weather modelling. The second is my original idea, which is applications of long-term climate modelling combined with conventional geospatial methods to identify areas of urban and rural insight.

&nbsp;  

### climateModelling

which is really more like weather modelling; This is most of the work we've done with the centre over the summer.
 
### Data

 - IMD has 1x1 temperature from 1951 to 2024 - which we've downloaded as ``heat_main``.
 - IMD has 2.5x2.5 temperature from June 2015 to 2024, which is about 9 years, which we've downloaded as ``heat_rt``. Is 9 years enough to draw meaningful inferences? It definitely isn't for climate, but maybe for weather?
 - [ERA-5 Reanalysis](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-complete?tab=form)
 - [ERA-5 hourly pressure data](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-pressure-levels?tab=form)
 - [Bhuvan DEM and other ISRO data](https://bhuvan-app3.nrsc.gov.in/data/download/index.php?c=s&s=C1&p=cdv2&g)
 - [Heat and moisture based heatwave maps](https://bhuvan-app1.nrsc.gov.in/heatwave/)
 - [NSRDB solar radiation data](https://developer.nrel.gov/docs/solar/nsrdb/)
 - [NSRDB datasets](https://nsrdb.nrel.gov/data-sets/international-data)
 - [IMDAA & NGFS Reanalysis](https://rds.ncmrwf.gov.in/)
 - Can use [OPeNDAP](https://www.opendap.org/) which could help with remotely accessing large datasets

### Lit Review

 - [Lit review presentation](https://www.canva.com/design/DAGKtv2ri6c/f_HtVsEyY5WYIoyXIgBkZg/edit)
 - [Lit review (Sapta)](https://github.com/kkkarnav/thesis/blob/main/presentations/Paper_Presentations%20(Sapta).pdf)
 - [Lit review (Divij)](https://github.com/kkkarnav/thesis/blob/main/presentations/Paper_Presentations%20(Divij).pdf)
 - [Work Report (Divij)](https://github.com/kkkarnav/thesis/blob/main/reports/Weather%20Modelling%20Report%20(Divij).pdf)

 - Data:
     - [IMD Lib] [IMDLIB: An open-source library for retrieval, processing and spatiotemporal exploratory assessments of gridded meteorological observation datasets over India](https://www.sciencedirect.com/science/article/abs/pii/S1364815223002554)
     - [NRSDB solar data] [NREL India Solar Resource Data](https://www.nrel.gov/docs/fy21osti/78025.pdf)
     - [Global weather station dataset] [WEATHER-5K: A Large-scale Global Station Weather Dataset Towards Comprehensive Time-series Forecasting Benchmark](https://github.com/taohan10200/WEATHER-5K?tab=readme-ov-file)
     - [Sentinel-2 terrain mosaics] [Sentinel-1 Monthly Mosaics in the Copernicus Data Space Ecosystem](https://dataspace.copernicus.eu/news/2024-8-6-announcing-sentinel-1-monthly-mosaics-copernicus-data-space-ecosystem)
     - [Harmonized Landsat Sentinel reflectance data] [HLSL30: HLS-2 Landsat Operational Land Imager Surface Reflectance and TOA Brightness Daily Global 30m](https://developers.google.com/earth-engine/datasets/catalog/NASA_HLS_HLSL30_v002)

 - Methods:
     - [Statistical overview] [Review of trend detection methods and their application to detect temperature changes in India - P. Sonali, D. Nagesh Kumar (2012)](https://www.sciencedirect.com/science/article/abs/pii/S0022169412009341?via%3Dihub)
     - [(tmax+tmin)/2 isn't a good estimate] [On the min–max estimation of mean daily
temperatures](https://bpb-us-w2.wpmucdn.com/sites.uwm.edu/dist/f/330/files/2019/10/Clim.-Dyn.-min-max.pdf)
     - [Stationarity & detrending] [Stationarity & detrending](https://www.statsmodels.org/dev/examples/notebooks/generated/stationarity_detrending_adf_kpss.html)
     - [Statistical trends in IMD data] [Spatial and Temporal Trends in High Resolution Gridded Temperature Data over India](https://link.springer.com/article/10.1007/s13143-019-00120-1)
     - [Normal distribution conversion of temperature] [On the statistical distribution of temperature and the classification of extreme events considering season and climate change—an application in Switzerland](https://link.springer.com/article/10.1007/s00704-023-04530-0)
     - [Indian rainfall analysis] [Characteristics of southwest summer monsoon rainfall events over East India](https://www.researchgate.net/publication/342165818_Characteristics_of_southwest_summer_monsoon_rainfall_events_over_East_India)
     - [Downscaling weather predictions with AI] [Emerging AI-based weather prediction models as downscaling tools](https://arxiv.org/pdf/2406.17977)
     - [Comparison of ML vs Numerical methods] [Do data-driven models beat numerical models in forecasting weather extremes? A comparison of IFS HRES, Pangu-Weather, and GraphCast](https://gmd.copernicus.org/articles/17/7915/2024/)
     - [Fine-tuning GraphCast] [Efficient fine-tuning of 37-level GraphCast with the Canadian global deterministic analysis](https://arxiv.org/abs/2408.14587)
     - [GraphCast is better than ECMWF for cumulative precipitation forecasting] [Evaluation of precipitation forecasting base on GraphCast over mainland China](https://www.researchsquare.com/article/rs-4645037/v1)
     - [NASA explainer on foundational models] [Will AI Foundation Models Transform Scientific Research?](https://ntrs.nasa.gov/api/citations/20230013275/downloads/AI%20FM%20Scientific%20Research.pdf)
     - [Fine-tuning Prithvi for LULC] [Finetuning the Geospatial Foundation model for Land Cover mapping](https://openreview.net/pdf?id=56567S7W9E)
 
 - Models:
     - [Aastha-Apoorv paper] [Comparing skill of historical rainfall data based monsoon rainfall prediction in India with NCEP-NWP forecasts](https://arxiv.org/pdf/2402.07851)
     - [Georgia NN weather prediction] [Artificial neural networks for automated year-round temperature prediction](https://sci-hub.se/http://dx.doi.org/10.1016/j.compag.2009.04.003)
     - [Climate induced disaster prediction] [Impact Analysis of Climate Change on Floods in an Indian Region Using Machine Learning](https://link.springer.com/chapter/10.1007/978-3-031-44198-1_31)
     - [Physical climate foundational model] [Improved Surface Temperature Prediction for the Coming Decade from a Global Climate Model - Smith (2007)](https://sci-hub.se/https://doi.org/10.1126/science.1139540)
     - [DL-based heatwave forecasts] [Deep Learning-Based Extreme Heatwave Forecast](https://www.frontiersin.org/journals/climate/articles/10.3389/fclim.2022.789641/full#F2)
     - [Ensemble of ML models] [Evaluation of five global AI models for predicting weather in Eastern Asia and Western Pacific](https://www.nature.com/articles/s41612-024-00769-0)
     - [Other paper by same Ensemble paper author] [Application of a weighted ensemble forecasting method based on online learning in subseasonal forecast in the South China](https://geoscienceletters.springeropen.com/articles/10.1186/s40562-024-00319-9)
     - [GraphCast for solar radiation prediction] [Solarcast-ML: Per Node GraphCast Extension for Solar Energy Production](https://arxiv.org/abs/2406.13559)
     - [GraphCast with uncertainty quantification included in predictions] [GraphCast-Qtf: An improved weather prediction model based on uncertainty quantification methods](https://ieeexplore.ieee.org/abstract/document/10660789)
     - [Pritvhi for flood mapping & prediction with satellite imagery] [Assessment of a new GeoAI foundation model for flood inundation mapping](https://arxiv.org/pdf/2309.14500)
    

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
 - [FuXi: Ensemble-mean based forecast model](https://www.ecmwf.int/en/about/media-centre/aifs-blog/2023/new-ml-model-ecmwf-web-charts)

### Benchmarks

 - [WeatherBench 2](https://blog.research.google/2023/08/weatherbench-2-benchmark-for-next.html)

### Ideas

 - Markov chains for weather prediction
 - Satellite images?
 - Look for satellite image inference literature

### People

 - [Thierry Roncalli, Evry Paris Saclay](https://research-center.amundi.com/thierry-roncalli)
 - [Christopher Subich, Environment Canada](https://scholar.google.ca/citations?user=EU99a0YAAAAJ&hl=en)

### To Do

 - Replicate the experiments
 - Figure out reanalysis
 - Use satellite image data products
 - Explore ISRO data

&nbsp;  

### pricingLand

which is not as clearly defined; This is most of the work I've been interested in doing geospatially.
 
### Data

 - BhuNaksha
     - Each state has a BhuNaksha instance which has point-accurate polyons of each plot of land. The [availability](https://bhunaksha.nic.in/bhunaksha/implementationstatus.jsp) is: Himachal, Haryana, Uttar Pradesh, Rajasthan, Maharashtra, Bihar, Odisha, Jharkhand, Chattisgarh, Andhra, Telangana, Goa, Kerala. The main missing states are Uttarakhand, Punjab, Gujarat (BhuLekh solution), WB, Karnataka, and Tamil Nadu.
     - [Magicbricks BhuLekh catalog](https://www.magicbricks.com/blog/state-wise-land-record-name-in-india/117824.html)
     - [Gujarat AnyROR (BhuLekh)](https://anyror.gujarat.gov.in/)
     - [Bengal's offline eBhuchitra](https://allowb.org/grad_pdfs/eBhuchitra_UserManual_FHTD_compressed.pdf)
     - [Bengal digitalized land records available at district offices](https://banglarbhumi.gov.in/BanglarBhumi/DigitisationMapRecords.action)
     - [Telangana "Dharani" (Bhunaksha)](https://dharani.telangana.gov.in/gis/)
     - [Haryana HSAC (Bhunaksha)](https://hsac.org.in/eodb/)
     - [Karnataka land records](https://landrecords.karnataka.gov.in/service3/)

 - Circle rates
     - [Bengal circle rates](https://wbregistration.gov.in/(S(g2iboa1ham2n323pn5zql0zs))/index/Search_By_Property_new.aspx?SearchingFrom=WS)
     - [Karnataka circle rates](https://bbmptax.karnataka.gov.in/documents/zone2008.aspx)
 
 - Other
     - [DILRMP dashboard](https://dilrmp.gov.in/)
     - [Bhoonidhi remote sensing data](https://bhoonidhi.nrsc.gov.in/bhoonidhi/)
     - [MOSPI catalogue](https://www.mospi.gov.in/sites/default/files/publication_reports/Compendium_15-09-2023_publishedv2.pdf)

### Lit Review

 - Land Records:
     - [Survey of the land record system] [Land Records and Titles in India](https://prsindia.org/policy/analytical-reports/land-records-and-titles-india)
 
 - Pricing:
     - [Survey of climate risk pricing] [Pricing of climate risks in financial markets: a summary of the literature](https://www.bis.org/publ/bppdf/bispap130.pdf)
     - [Survey of climate risk-adjusted portfolio construction] [Portfolio Construction with Climate Risk Measures](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3999971)
     - [Real estate climate risk factor] [Measuring Climate Risk in Real Estate Portfolios](https://www.msci.com/www/blog-posts/measuring-climate-risk-in-real/01973063966)
     - [How firms acquire land parcels] [Land Market Frictions in Developing Countries: Evidence from Manufacturing Firms in India](https://aradhyasood.github.io/Land_Frictions_Manufacturing_India_Sood%281%29.pdf)

 - Elevation:
     - [Building DSM based on lidar] [Using LiDAR to map tree shadows](https://tedpiotrowski.svbtle.com/using-lidar-for-tree-shadows-in-shademap)
     - [Transformer and lidar based tree height prediction] [Very high resolution canopy height maps from RGB imagery using self-supervised vision transformer and convolutional decoder trained on aerial lidar](https://www.sciencedirect.com/science/article/pii/S003442572300439X)
     - [Individual tree shading model] [From Dawn to Dusk: High-Resolution Tree Shading Model Based on Terrestrial LiDAR Data ](https://www.mdpi.com/2072-4292/16/12/2189)
     - [How to build a DSM from lidar] [USC Urban Tree Shade Model](https://storymaps.arcgis.com/stories/7f5c570fa0ff4d2eb918f933d869a2d6)
 
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
 - [Aradhya Sood, Toronto](https://sites.google.com/view/aradhyasood)

### To Do

 - 

&nbsp;  

### Resources:

 - [statsmodels](https://www.statsmodels.org/dev/examples/index.html)
 - [Intro to Python GIS](https://automating-gis-processes.github.io/CSC/index.html)
 - [Forecasting: Principles & Practices](https://otexts.com/fpp2/index.html)
