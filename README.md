# A Gentle Introduction to "Swarm of Micro Flying Robots in the Wild"

## Motivation and Inspiration

_Chao Xu and Fei Gao:_ As researchers gradually discovered the secrets of ants foraging on pheromones and bees using dance to identify nesting sites in the 1980s, swarm intelligence has become a widely studied topic. **Many researchers** have proposed effective coordination schemes by observing the behavior of animal groups and verified them on real robots, but these algorithms perform mainly in structured environments. With the rapid development of sensor and computing technology in recent years, robot swarms have emerged all-around, such as warehousing robots, logistics robots, autonomous driving, etc. 

_Chao Xu and Fei Gao:_ To find a solution that functions not only in structured environments, but also natural environments, **unlike traditional multi-agent algorithms** that design sophisticated interaction rules, we choose to achieve swarm intelligence by pushing the boundary of high-level single-robot autonomy. So we focused on single-robot navigation for many years until we successfully made our aerial robots fly out of the laboratory and fly into challenging environments such as forests, streets, indoors, and underground tunnels. Then we know it's time for aerial swarms.

_Chao Xu and Fei Gao:_ **Our interest in swarm robotics** stems from science fiction movies. As a symbol of high technology, aerial swarms often represent the future world. So we are always thinking about what we can do to take this step into the future.

_Xin Zhou:_ To achieve this future through aerial swarms, we first have to solve the **TEEM** problem. Imagine a forest search and rescue scenario where we need to search for missing persons. 
1. Time is life, and the swarm needs to plan smooth and fast trajectories to cover as much area as possible within a limited time. This is trajectory optimality. 
2. Performing the search and rescue missions needs to consider a variety of requirements. In addition to energy efficiency, dynamic constraints, obstacle avoidance, etc., it may also be necessary to consider reducing repeated searches, changing search accuracy in different areas, and so on. A variety of task requirements should be handled by the system framework with a unified workflow as much as possible. That's what extensibility means.
3. Economical computing is the key to deploying algorithms on embedded computers, which robots can therefore carry.
4. Miniature size means the robot travels through narrower gaps and flies into more restricted areas. This is necessary to search for missing people in dense woods where even people can't walk smoothly.

_Xin Zhou:_ Unfortunately, achieving these four aspects together is internally contradictory and therefore, **difficult**. Higher optimality mostly comes from sophisticated modeling and more iterations or trials in the solution space, all of which are achieved at the cost of increased computing time. Higher extensibility requires the problem to be defined in a more general form at the sacrifice of potential problem-specific optimization that can improve optimality and reduce computing time. Then, between optimality and extensibility, as various user-defined objectives are imposed, the problem becomes increasingly complex, which makes it challenging to find a solution.

## Methodology

_Xin Zhou:_ In our system, each robot is **equipped with a stereo camera, attitude sensor and embedded computer**. The computer uses image and attitude data for localization. It uses the stereo camera to observe the surrounding obstacles, and obtain areas. Based on this, the trajectory planning module will plan a trajectory immediately that will neither hit obstacles nor other robots in the next few seconds. The controller then controls the propellers to follow this safe trajectory. The above process is repeated, and the entire swarm continues to run.

_Fei Gao:_ Our work was **inspired by birds** that fly smoothly in a free swarm through even very dense woods. We observe that, birds’ vision and brain capabilities allow them to pass through the gaps between trees accurately and quickly. There is no doubt that, the sensing and processing capabilities of vision and brain play a critical role in this scenario. Our aerial robots are equipped with stereo cameras and onboard computers, which allow them to precisely understand the environments and plan nice trajectories. Also, they share information among the group and cooperate with others, to mimic swarm flight of birds in natural challenging environments. 

_Fei Gao:_ We conduct experiments to validate our system in **Zhejiang province, China**. In the multi-robot tracking experiment, four robots were used. In all the other three experiments, 10 robots flew simultaneously.

_Fei Gao:_ To achieve our desired autonomy and miniaturization, we **designed and manufactured** all of the robots ourselves.

_Fei Gao:_ Regarding **wireless communication**, an important property of our system is trajectory-based communication. An unlimited number of position points can be acquired on a trajectory, only the time needs to be entered. Compared with location-based communication, our method greatly improves the information density.

## Potential Implementations and Future Works

_Fei Gao:_ Based on the proposed platform, **we are going to** study on large-scale coordination, flexible formation, efficient task assignment, navigation in harsh environments, etc. Maybe it’s time for people worldwide that can start thinking about how to make good use of the infinite space above our heads, make air transportation a reality, and save every possible life in disasters.

_Fei Gao:_ We feel that the **possible applications** of our algorithms and systems are so broad that any field that requires UAV navigation, including single robot and swarms, is available. For us, **swarm is an extension of a single robot**. It can exponentially improve the efficiency of task execution, and can also realize functions that a single robot cannot complete. As we said in Introduction, from rescuers, to animal and plant researchers, and even each of us expecting aerial traffic in the future, will receive the benfits. We believe that we will all benefit from this algorithm and system.

_Fei Gao:_ As far as we know, some companies are already developing and testing aerial logistics based on aerial swarms in cities, of course, mainly for small goods. We believe that we will receive packages delivered by aerial robots to our balconies **in the next five years.**
