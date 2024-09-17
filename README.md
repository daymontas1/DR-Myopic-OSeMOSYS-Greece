This repository contains the files for simulations that evaluate the impact of short-term bias and temporally-inconsistent preferences on the cost-optimal configuration of the power sector. The simulations model a consecutive decision-making process with a rolling one-year forward-looking window. In each time step, the social planner reassesses future years from a perspective that advances by one year. Furthermore, the simulations utilize two discount rate curves: one exponential and one logarithmic. Both curves reflect a declining interest in the future by decision-makers as time progresses, but the latter does so at a more rapid rate. Moreover, two decarbonization mechanisms are examined, carbon prices and an emission budget. This time-inconsistent framework is implemented in a linear programming optimization model representing the power sector of Greece with a technological detail from 2019 to 2070 (the model is described in: Koutsandreas, D., Trachanas, G. P., Pappis, I., Nikas, A., Doukas, H., & Psarras, J. (2023). ''A multicriteria modeling approach for evaluating power generation scenarios under uncertainty: The case of green hydrogen in Greece.'' Energy Strategy Reviews, 50, 101233.). 

To reproduce the simulations, first the desired scenario must be selected. 'Carbon_prices(Ref1)' folder contains scenarios involving carbon prices, while the 'Emission_Budget(Ref2)' folder contains scenarios involving an emission budget. In these folders, the 'Exponential' folder contains scenarios with an exponentially increasing discount rate, and the 'Logarithmic' folder contains scenarios with a logarithmically increasing discount rate. In the scenario file names, the year X after the underscore (''_X'') represents the base year of the model, at which investment decisions are taken. The selected scenario must be renamed as 'data', replacing the existing data file in the main folder. Following, the scenarios can be simulated using the executable file (.exe). A GLPK or CPLEX solver is required to solve the scenarios, while simulation results will be stored in the 'res' folder.
