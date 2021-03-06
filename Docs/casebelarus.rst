.. _casebelarus:

Dispa-SET for the Belarus
=========================

Description
-----------
Planning the future: Integrating renewable energy sources in the Belarusian power system

Background
----------
The Belarusian energy sector is mainly running on fossil fuels. Approximately two third of the country’s energy production is covered by natural gas, which is mainly imported from Russia. Therefore, increasing the share of renewables in the energy balance has become one of the priority areas of the economic policy of the Belarusian government. In this regard, the objective of this work is the development of smart power and heating systems that can handle increased shares of renewable energy in the Belarusian system. This research focuses on several aspects such as balancing issues, flexibility requirements and congestion management in Belarusian grid. 
 
Methods and Features
--------------------
The Belarusian energy system has been modeled in Dispa-SET, an open-source unit commitment and optimal dispatch model focused on the balancing and flexibility problems in European grids. A reference and several future scenarios with high share of renewable energy sources were created. This case study analysis provides insights on the ability to integrate as much renewables as possible into the system and to check its impact on the price of runing the system.

The model is expressed as an optimization problem. Continuous variables include the individual unit dispatched power, the shedded load and the curtailed power generation. The binary variables are the commitment status of each unit. The main model features can be summarized as follows:

- Minimum and maximum power for each unit
- Power plant ramping limits
- Reserves up and down
- Minimum up/down times
- Load Shedding
- Curtailment
- Pumped-hydro storage
- Non-dispatchable units (e.g. wind turbines, run-of-river, etc.)
- Start-up, ramping and no-load costs
- Multi-nodes with capacity constraints on the lines (congestion)
- Constraints on the targets for renewables and/or CO2 emissions
- Yearly schedules for the outages (forced and planned) of each units
- CHP power plants and thermal storage

The demand is assumed to be inelastic to the price signal. The MILP objective function is therefore the total generation cost over the optimization period. 

Quick start
-----------

If you want to download the latest version from github for use or development purposes, make sure that you have git and the [anaconda distribution](https://www.continuum.io/downloads) installed and type the following::

	git clone https://github.com/energy-modelling-toolkit/Dispa-SET.git
	cd Dispa-SET
	conda env create  # Automatically creates environment based on environment.yml
	source activate dispaset # in Windows: activate dispaset
	pip install -e . # Install editable local version

The above commands create a dedicated environment so that your anconda configuration remains clean from the required dependencies installed.

To check that everything runs fine, you can build and run a test case by typing::

	dispaset -c ConfigFiles/ConfigTest.xlsx build simulate

Make sure that the path is changed to local Dispa-SET folder in folowing scripts (the procedure is provided in the scripts)::

	build_and_run.py
	read_results.py

  
Documentation
-------------
The general documentation of the Dispa-SET model and the stable releases are available on the main Dispa-SET website: http://www.dispaset.eu

Licence
-------
Dispa-SET is a free software licensed under the “European Union Public Licence" EUPL v1.2. It can be redistributed and/or modified under the terms of this license.

Results
-------
In this model the potential for integration of renewables in the power system of Belarus was examined. The results of this study indicate that the current grid infrastructure can utilize up to 30% of the energy generated by renewables without causing any balancing and stability issues while applying heat pumps, thermal storage and bio-waste-based technologies.

Conclusions
-----------
The analysis performed in this work has demonstrated that the utilization of renewables could greatly reduce the use of fossil fuels and hence reduce the annual CO2 emissions by about 5 million tons in the Belarusian energy sector. This way the high dependence on external energy markets should decrease. The designed scenarios should help to realize a Belarusian Energy and Environmental Policy where the share of renewables should reach 30%.


Highlights
----------

.. .. image:: figures/Balkans_capacity.png

.. .. image:: figures/Balkans_generation.png

Main developpers
----------------
- Matija Pavičević (KU Leuven) - gathered and analysed the data, performed the computations, analysed and verified the results
- Darya Muslina (Belarusian National Technical University) - gathered and analysed the data
- Yuliya Stanetskaya (Belarusian National Technical University) - gathered and analysed the data

References
----------
More details regarding the model and its implementation are available in the following publications



