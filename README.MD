# Extended PySWMM

Extended SWMM5 API for optimization problems

## Original API: 

[PySWMM](https://github.com/OpenWaterAnalytics/pyswmm) - Open Water Analytics 


## What's new? 

Add features to manipulate the link cross-sections. Changing diameters and type of your conduits. 

See in swmm5.py: 

1. Property getters:

		getLinkLength()
		getLinkXsectDiameters()
		getLinkType()

2. Property setter:

		setLinkXsectDiameters() 

## Usage 

The **lib/linux/swmmapi_extended.so** is compiled from modified C source code [**SEE HERE**](https://github.com/NikoZHAI/Stormwater-Management-Model). 

One should load this executable when you want to use the above-stated features.

	import pyswmm as swm
	with swm.Simulation(inputfile='my_inp.inp', swmm_lib_path='pyswmm_ROOT/lib/linux/swmmapi_extended.so') as sim:
		# Example usage
		l = sim._model.getLinkLength(link_index)
		print(l)

## Related Project

Multi-objective optimization by progressive improvement of surrogate machine learning models (MOPRISM) 

hosted by UNESCO-IHE 

supervised by Prof. Dimitri Solomatine and Dr. Juan Carlos Chacon-Hurtado

## Contact 

Huanyu ZHAI - huanyu.zhai@outlook.com
