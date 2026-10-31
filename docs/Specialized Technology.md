# Specialized Technology & Fundamental Concepts 

C1 Fundamental Concepts
- Machine Learning (ML): the computer learns patterns from past data instead of following fixed rules written by a programmer.
- Supervised learning: the model learns from past bus trips where the actual travel time between stops is already known.
- Regression: the model predicts a number, which here is the minutes until the bus arrives.
- Features (inputs): hour of day, day of week, route, distance, rain, current bus speed.
- Data: GTFS Static (timetable) and GTFS Realtime (live bus GPS every 30 seconds) from data.gov.my.
- How it works: collect data → clean → train model → test → predict live arrival times.
- Evaluation: Mean Absolute Error (MAE), the average difference between predicted and actual time.

C2 Methods and Tools
| Name | Use in this project |
|------|---------------------|
| Linear Regression	| Simple baseline model for predicting travel time |
| Random Forest |	Main model; handles complex patterns like peak hour + rain |
| scikit-learn | Python library to train and test the models |
| pandas | Python library to clean the data and create features |


C3 Fit to the Problem
- How it helps: ML can predict the arrival time at each bus stop, which MyRapid PULSE currently does not show reliably.
- Benefits
  - Uses existing open data, so no new hardware is needed
  - Learns real traffic patterns that a fixed timetable ignores
- Limitations
  - Live data sometimes has gaps, which can cause wrong predictions
  - Accidents and road closures are hard to predict from past data
- Alternative : show only the timetable. It is simple and cheap, but ignores traffic delays.
- Choice : ML, with the timetable as a backup when live data is missing. (reason to be added)
