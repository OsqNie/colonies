# Colonies
An agent-based model for simulating economics and material supply chain between space colonies

In this project we will create a rather simple look at economics between space colonies using an Agent-based model (ABM). ABMs are systems where individual organisms called agents follow a set of rules over a duration of a simulation. Mathematical simulations are often based on a set of equations describing an equilibrium of a system and studying effects leading to that point. ABMs by contrast work individually, often giving form to more complex phenomena if the agents are correctly set. This enables us to observe _emergence_ or the _"whole is greater than the sum of its parts"_ effect for complex systems.

This simulation creates a simplified universe with *planets* and *colonies*, each of which is situated in a 2d space. We want to study how constraints on diminishing resources create a network of trade in this universe. The universe consists of only two materials

- Commonium, a common material that is videly available on planets and is relatively cheap
- Importatium, a relatively rare mineral that is used for high-tech development

Additionally, each planet and colony will have the following traits

- Habitability, a number between 0 and 100. The number represents how hostile the area is for permanent settlementation, either by humans or automata. Each unit of habitability under 100 increases the cost of running the settlement. Money can be spent to increase habitability of the area. Habitability decreases with consumption of resources.
- Cost of operation: Cost to run the station, derived from habitability. Commonium and importantium are consumed for each person in the system.
- Population. Population consumes resources and creates wealth for the planet. 
- Capital, the number of machinery on the planet. Capital is increased over time with a known constant.
- Production. We will assume each planet porudces nothing but spaceships. A long shot, but this is a simple model. 

We use Cobb-Douglas productivity model (https://assets.aeaweb.org/asset-server/journals/aer/top20/18.1.139-165.pdf) of $Y = AK^\alpha L^\beta$, where $Y$ is the production output, $A$ is the scaling factor (often denoted productivity or technological prowess, which grows steadily over time), $K$ the amount of capital, $L$ the labour (equal to the population in our simulation) and $\alpha, \beta$ are constants for how much the output grows when one unit of capital or labor are added. Cobb and Douglas used values of $\alpha = 1/4, \beta = 3/4$ so we will run with those. A certain level of production is needed for spaceships, and spaceships wear down with time. They allow transportation of goods and people between planets. Spaceships have the following traits:

- Cargo: We assume 10 tonnes of payload, with each person and his belongings weighting a tonne.
- Cost to operate: a fixed sum of capital needed to run the spaceships
- Speed: how long it takes to reach each planet or settlement

The model is simple, so we will ignore most real-world restrictions. For example, we ignore the movement of planets, live on a 2d plane and disregard politics and sociology. We assume that the only motivation for humankind is to increase production indefinitely. The model aims to give a glimpse on how restricted resources give rise to colonies and the traffic flow between them

_The project is still early in developement. World building works as of February 2020, with animation capabilities and proof of concept preliminary models coming soon._
