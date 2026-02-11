# Extended Intelligence II: Mood-Boosting Song Agent {: .master-title}


# The Concept {: .master-title}

The initial concept was to create a kind of weather-radio AI agent. We started by reflecting on how weather conditions affect our moods, especially in winter when we might experience low energy, and whether we could personalize music recommendations to boost our moods.  So, our agent would recommend mood-boosting music based on weather data. This is the first draft of the dataflow and components:

![draft](../images/flow.jpg)

Given the challenges of the course to connect physical local information to AI agents, we decided to incorporate environmental sensing, at least one small aspect of it: light. So the final concept was: An OpenAI-based agent that recommends music based on weather data that gathers from a local light sensor and web search tools . 

We used an LDR sensor to measure the ambient light level in the environment.  The sensor gives analog light intensity values: lower values = darker environment, and higher values = brighter environment. This data was captured using a Raspberry Pi Pico and MicroPython.  Overall, the system consisted of a 3-agent workflow as shown in the diagram below, including the prompts for each one. 

![system](../images/agent%20diagram.jpeg)

![pico](../images/pico.jpeg)

# Reflection {: .master-title}

Overall, although I lack previous knowledge of AI agents and I’m only starting to learn about sensors, I was really excited about the possibility of connecting AI agents with local physical information. I have two areas where I would like to explore further 

__Expanding Environmental Sensing Capacity__

In the current prototype, the agent relies on a light sensor (LDR) and web-based weather data. While this already establishes a bridge between physical sensing and AI interpretation, the system could evolve into a more embodied and granular environmental listener by adding sensors of humidity, temperature, wind speed, etc. 
Adding more sensors wouldn’t be for the sake of making a more complex system but so that the agent could build a more accurate environmental mood model and have a higher probability that its recommendation actually improves the user’s emotional state. It is about reducing ambiguity. For example, low light could mean a cozy evening or a depressive winter afternoon, and cold temperature could feel refreshing or uncomfortable depending on humidity and wind. Of course we would need more research to reflect on wheather environmental data truly predict individual mood reliably.

__An emotional forecast of weather__

In a world where strive to sense, feel and empathize with climate projections, maybe sound – in the form of music – could be a means to generate empathy. Embodying sonic worlds that are attuned to future weather conditions is an exciting future direction I would like to try!

The AI agent could use climate models for 2050 or 2100, especially take into account increased average temperatures, more extreme weather events in specific areas. In this way, the agent could generate music for a summer day in 2050 during a heat wave, a winter day that feels like summer, etc. And there are other parameters of design that would be interesting, for example instead of matching future weather scenario to a mood-boosting song, the agent could predict how future climate might affect collective mood and play a song that represents the mood of that future citizen. For example, increased heat → irritability → more aggressive music. Music would be a window into emotional states of the future. And users in the present could embodied those future selves. 


