# Sample Fitness Polar Dataset

This dataset comes from real data from my Polar user, which represents 8 of my training years. Note that I have modified some of the data in order to remove some pre-calculated metrics because this dataset's purpose is to teach some of my students.

The original dataset was downloaded by following the steps described [here](https://support.polar.com/en/how-to-download-all-your-data-from-polar-flow).

Since these data are not well documented, I decided to mention some features that may help you. Do note that most of the file structure is self explainable and it is all in JSON format.

- The ``exercises`` field is a list, but it always has size 1. This is used for sessions with multiple sports in it, like duathlon or triathlon. These are not exercises I practiced in 2016, so there will always be only one exercise in here.

- The ``zones`` field indicates the zones for some metrics. Specially heart rate and speed zones. Why do these divisions exist? Depending on the zone the athlete is performing, the benefits to the human body are different. This is why they exist. The task to find out which benefits each zone provides is up to you.

- The ``samples`` field is one of the most important. It has instant measures for each metric with a timestamp. In 2016, the Polar watch I used (Polar M400) performed one measurement around every 1 second. The ``heartRate`` field values are in beats per minute. The ``speed`` field values are in kilometers per hour. The ``altitude`` and ``distance`` fields are all in meters. The ``distance`` ``value`` fields are cumulative. You may use the ``recordedRoute`` to see the full route on that session.

- The ``weather dataset`` folder contains some weather info only about sessions with GPS data, based on the starting latitude and longitude coordinates. These data came from [visualcrossing service](https://visualcrossing.com/), so it is easy to find documentation about it. The query used to get these data used the ``unitGroup`` as ``metric``. I have provided json and csv files. Use whichever you prefer.

Note that some of these fields may be absent depending on the exercise provided in the file. Some times, I did not wear the heart rate sensor (there is no heart rate data), sometimes I forgot to enable the GPS (there is no GPS, speed, distance data) and so on. Some modalities just do not have some data by definition, for example, the ``strength training`` sessions are just simple workouts on the gym. They do not have GPS data and some of them may not even have heart rate data. Another example is the ``swimming`` sessions. In 2016 I used to swim in an inside pool, so I was not able to use the GPS, although I was able to count how many laps I made on the pool and I manually typed the total distance, so it is possible to find sessions with a total distance, but no GPS data.

You may want to read some texts to familiarize yourself with some metrics. Google about what most fitness watches provide about speed, pace, heart rate zones, what to measure on each kilometer of a session, metrics from the first 5km/10km in a session etc. Be creative on what you can calculate and how to visualize them. Remember that replicating what already exists may be interesting, but you need to go beyond to stand out.

This dataset is meant to be used as a challenge. The data is not the same in all the files and you must study them in order to understand how to process them. Hey, this is the real world!

If you want to use this dataset for self study, classroom or whatever you want to do with it, I just ask you to add a reference to this repo.

Also, feel free to follow me on [Polar Flow](https://flow.polar.com/training/profiles/3142224), [Strava](https://www.strava.com/athletes/9485255) and [Instagram (@mendi_km)](https://instagram.com/mendi_km). You may search for some of these sessions on these platforms to compare your results.

Good luck on the challenge you have been assigned!
