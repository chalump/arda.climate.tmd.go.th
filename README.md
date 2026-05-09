# tmd-arda-s2dfs-dashboard
# ARDA S2DFS System
# Seasonal to Decadal Forecasting System (S2DFS) and Climate Risk Decision Support Platform
# Overview

The ARDA Seasonal to Decadal Forecasting System (S2DFS) is an integrated climate prediction and decision-support platform developed to enhance Thailand’s capability in climate forecasting, disaster-risk reduction, and climate-service delivery. The system combines statistical climate forecasting techniques, geospatial analysis, probability-based outlooks, and operational visualization tools into a unified platform for monitoring and decision-making. The primary focus is on seasonal rainfall prediction, drought and flood risk assessment, and climate-informed planning at national and sub-national scales.

The platform integrates climate predictors such as Sea Surface Temperature (SST), atmospheric circulation patterns, and large-scale climate variability with observed rainfall and hydrological datasets. The outputs are transformed into operational products including rainfall outlooks, SPI drought indicators, exceedance probabilities, risk classifications, and decision-guidance recommendations. The system is designed to support operational agencies, researchers, water managers, agricultural planners, and local stakeholders.

The dashboard framework allows users to interactively visualize geospatial products at multiple administrative and hydrological scales, including provinces, districts, river basins, and sub-basins. The platform also supports contextual diagnostics, local distribution analysis, operational guidance generation, and exportable reports. The system aims to strengthen climate resilience, improve preparedness, and support evidence-based policy and operational planning under changing climate conditions.

# Main Objectives

The primary objective of the ARDA S2DFS System is to develop an operational Seasonal to Decadal Forecasting framework capable of providing climate outlooks and climate-risk information for Thailand. The system is intended to bridge the gap between climate science and practical decision-making by translating climate forecasts into actionable risk information. This includes improving the accessibility and usability of climate services for multiple sectors including agriculture, water management, disaster management, and urban resilience.

Another major objective is to improve early warning and climate-risk monitoring capabilities at regional and local scales. The system integrates climate anomalies, drought indices, rainfall probabilities, and risk classifications to provide operational guidance and preparedness recommendations. Through the use of geospatial visualization and polygon-based aggregation, the system can identify vulnerable areas and support area-specific planning and adaptation measures.

The project also aims to investigate the mechanisms and drivers of climate variability affecting Thailand. Large-scale climate phenomena such as ENSO, monsoon variability, and SST anomalies are analyzed and linked to rainfall variability and hydrological extremes. These analyses improve forecasting skill and provide scientific understanding of climate-related risks.

Finally, the system aims to establish an operational climate-service platform capable of disseminating research outputs, climate products, risk assessments, and forecast guidance to end users through interactive dashboards and digital services.

# System Architecture

The S2DFS architecture is designed as a multi-stage workflow integrating climate data processing, statistical modeling, geospatial analysis, and interactive visualization. The workflow begins with climate data acquisition and preprocessing, including quality control, anomaly calculation, temporal aggregation, and spatial harmonization. Multiple datasets from satellite observations, reanalysis products, and climate datasets are standardized into a unified analysis framework.

The forecasting component uses statistical and multivariate methods including EOF, PCA, and CCA to identify relationships between climate predictors and rainfall predictands. The forecasting workflow extracts dominant climate modes, projects them into canonical space, and generates probabilistic seasonal forecasts. These forecasts are then evaluated using skill metrics such as correlation, RMSE, and MAE through cross-validation approaches.

The risk-assessment component converts forecast products into operational risk indicators such as SPI drought severity, exceedance probability, and flood/drought/agriculture risk classes. Spatial aggregation is performed using administrative and basin polygons to support local interpretation and decision-making. The outputs are exported into lightweight JSON and GeoJSON formats optimized for dashboard rendering.

The final stage is the visualization and decision-support layer. Interactive dashboards display forecast maps, local diagnostics, ranking tables, guidance panels, and contextual overlays. Users can interactively select polygons, explore local distributions, compare probabilities, and export operational reports. The system architecture is modular and scalable, allowing future integration with hydrological models, AI-based forecasting systems, and real-time climate services.

# Climate Forecasting Module

The climate forecasting module forms the scientific core of the S2DFS platform. It uses multivariate statistical methods to identify the dominant relationships between large-scale climate variability and rainfall patterns over Thailand. The forecasting framework is based primarily on Canonical Correlation Analysis (CCA), which is capable of linking predictor fields such as SST anomalies with rainfall predictands while maximizing the explained covariance between the two datasets.

The preprocessing stage includes anomaly calculation, climatological normalization, EOF decomposition, and dimensionality reduction. Empirical Orthogonal Function (EOF) analysis is used to identify dominant spatial modes of variability, while Principal Component Analysis (PCA) extracts temporal coefficients representing large-scale climate signals. These reduced predictor and predictand fields are then used in the CCA framework to establish canonical relationships.

The forecasting system supports lagged predictor analysis, allowing SST conditions from earlier months to predict future rainfall conditions. This enables seasonal forecasting applications with lead times ranging from one to several months. The model can also be extended toward decadal variability analysis using longer-term climate signals and low-frequency climate modes.

Model validation is performed using Leave-One-Out Cross Validation (LOOCV) and skill verification metrics. Forecast skill maps are generated spatially to identify regions with stronger predictive capability. These verification products are critical for operational interpretation and confidence assessment.

# Forecast Products

The S2DFS platform generates a comprehensive suite of climate forecast and risk-analysis products. These products are designed to support both scientific analysis and operational decision-making. Forecast outputs include actual rainfall predictions, rainfall anomalies, and percentage anomalies relative to climatological baselines. These products provide direct interpretation of expected wet or dry conditions for the target season.

Drought monitoring products are generated using the Standardized Precipitation Index (SPI) at multiple time scales. SPI-1 is used for short-term moisture stress monitoring, SPI-3 represents seasonal conditions, and SPI-6 reflects longer-term hydrological and agricultural drought conditions. These indices help identify both emerging and persistent drought situations.

The platform also generates probability-based outlooks including tercile probabilities (above-normal, near-normal, below-normal rainfall), heavy-rain probability, and exceedance probabilities such as P67, P85, and P95. These products provide probabilistic interpretation of climate risks and improve communication of forecast uncertainty.

Risk products integrate multiple indicators into operational classifications including flood risk, drought risk, agriculture risk, and advisory classes. These products support early warning, preparedness planning, and climate-risk communication. The outputs are visualized through interactive geospatial maps and integrated into the decision-guidance framework.

# Spatial Aggregation and Geospatial Analysis

The system supports multi-scale spatial aggregation using administrative and hydrological polygon layers. Forecast and risk products are aggregated over provinces (ADM1), districts (ADM2), main river basins, and sub-basins. This polygon-based aggregation allows climate information to be translated into operational units relevant for planning and management.

Geospatial analysis includes polygon clipping, area-weighted averaging, and spatial overlay operations. Raster climate products are converted into polygon summaries through spatial aggregation methods optimized for operational dashboard performance. These methods ensure consistency between raster-based forecasts and polygon-level interpretations.

The platform also supports contextual overlays such as basin boundaries, administrative hierarchies, and risk zones. Selected polygons can be dynamically highlighted with local overlays, neighboring boundaries, and contextual diagnostics. This improves local interpretation and allows users to explore climate conditions within specific regions.

GeoJSON products are optimized for web visualization and dashboard interaction. Simplified polygon geometries and cached spatial processing are used to improve rendering performance while maintaining geographic consistency. These optimizations are critical for operational deployment and user interaction.

# Dashboard and Visualization System

The S2DFS dashboard is an interactive web-based climate-service platform designed for operational visualization and decision support. The dashboard integrates forecast maps, SPI products, probability outlooks, risk indicators, skill verification layers, and guidance panels into a unified interface. The design prioritizes clarity, operational usability, and rapid interpretation of climate information.

Users can interactively select months, products, and polygon layers. Clicking a polygon updates contextual diagnostics including local distributions, nearby polygons, risk interpretation, and guidance recommendations. The system also supports export functions for figures and one-page summary reports.

Visualization products are organized into thematic groups including forecast outlooks, SPI monitoring, probability layers, risk assessments, and skill verification. Each group contains interactive geospatial maps with consistent styling and operational color schemes. Polygon labels are dynamically filtered to reduce overlap and improve readability.

The dashboard also includes contextual interpretation panels for water management and agriculture guidance. These guidance panels translate climate signals into operational recommendations related to drought preparedness, reservoir operations, crop planning, irrigation management, and monitoring activities.

# Decision Guidance System

The decision-guidance system converts climate forecasts and risk indicators into actionable recommendations for operational planning. The guidance framework combines rainfall anomalies, SPI conditions, exceedance probabilities, probability terciles, risk classes, and forecast skill into integrated interpretation categories. This approach allows users to move beyond raw forecast data toward operational decision-making.

The guidance system uses alert categories such as DRY, WATCH, and LOW-MODERATE to communicate risk severity and preparedness levels. These categories are derived from combined indicators rather than a single variable. For example, a DRY classification may occur when below-normal rainfall probability is high, SPI conditions are negative, and drought risk indicators exceed operational thresholds.

Water-management guidance focuses primarily on SPI-1 and SPI-3 because water operations typically require short-term and seasonal-scale interpretation. Agriculture guidance includes SPI-6 because crops and soil moisture respond to longer-term moisture persistence. The guidance system also incorporates heavy-rain probability and exceedance indicators for flood preparedness.

Operational recommendations include monitoring strategies, reservoir management, irrigation planning, drought preparedness, crop adjustment measures, communication strategies, and coordination with disaster-management agencies. These recommendations are dynamically updated according to the selected polygon and forecast conditions.

# Technologies and Data Sources

The ARDA S2DFS platform is developed primarily using Python-based scientific and geospatial libraries. Core analysis components use xarray, pandas, numpy, scipy, scikit-learn, geopandas, and rasterio for climate-data processing and geospatial analysis. Statistical modeling workflows use EOF/PCA/CCA techniques implemented through Python scientific computing frameworks.

Visualization and dashboard components are implemented using HTML, CSS, JavaScript, and Plotly. Interactive geospatial rendering is performed using lightweight GeoJSON products optimized for browser-based visualization. Export functions support generation of PNG figures and operational summary reports.

The system integrates multiple climate and geospatial datasets including ERSSTv5, ERA5 reanalysis, CHIRPS rainfall, station observations, and Thailand administrative boundaries. Basin and sub-basin datasets are also integrated to support hydrological interpretation and basin-scale climate services.

The modular architecture allows future integration with AI/ML forecasting systems, hydrological models, cloud-based climate services, and real-time operational APIs.
