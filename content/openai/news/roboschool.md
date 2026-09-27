Title: Roboschool

URL Source: https://openai.com/index/roboschool

Markdown Content:
# Roboschool

We are releasing Roboschool: open-source software for robot simulation, integrated with OpenAI Gym.

![A 3D render of a robot and assorted limbs running along a track](https://images.ctfassets.net/kftzwdyauwt9/0bfeb6bf-4a8d-4073-dbc357afd9c1/73b0e3b539c67f6d9b6e65bf16a12aaf/roboschool.jpg?w=3840&q=90&fm=webp)

Roboschool provides new OpenAI Gym environments for controlling robots in simulation. Eight of these environments serve as free alternatives to pre-existing MuJoCo implementations, re-tuned to produce more realistic motion. We also include several new, challenging environments.

Roboschool also makes it easy to train multiple agents together in the same environment.

After we launched [Gym(opens in a new window)](https://gym.openai.com/), one issue we heard from many users was that the [MuJoCo(opens in a new window)](https://mujoco.org/) component required a paid license (though MuJoCo recently added [free(opens in a new window)](https://www.roboti.us/license.html) student licenses for personal and class work). Roboschool removes this constraint, letting everyone conduct research regardless of their budget. Roboschool is based on the [Bullet Physics Engine(opens in a new window)](http://bulletphysics.org/), an open-source, permissively [licensed(opens in a new window)](https://github.com/bulletphysics/bullet3/blob/master/LICENSE.txt) physics library that has been used by other simulation software such as [Gazebo(opens in a new window)](http://gazebosim.org/) and [V-REP(opens in a new window)](http://www.coppeliarobotics.com/).

Roboschool ships with twelve environments, including tasks familiar to Mujoco users as well as new challenges, such as harder versions of the Humanoid walker task, and a multi-player Pong environment. We plan to expand this collection over time and look forward to the community contributing as well.

For the existing MuJoCo environments, besides porting them to Bullet, we have modified them to be more realistic. Here are three of the environments we ported, with explanations of how they differ from the existing environments.

You can find trained policies for all of these environments in the `[agent_zoo](https://github.com/openai/roboschool/tree/master/agent_zoo)` folder in the GitHub repository. You can also access a `[demo_race](https://github.com/openai/roboschool/blob/master/agent_zoo/demo_race2.py)` script to initiate a race between three robots.

In several of the previous OpenAI Gym environments, the goal was to learn a walking controller. However, these environments involved a very basic version of the problem, where the goal is simply to move forward. In practice, the walking policies would learn a single cyclic trajectory and leave most of the state space unvisited. Furthermore, the final policies tended to be very fragile: a small push would often cause the robot to crash and fall.

We have added two more environments with the 3D humanoid, which make the locomotion problem more interesting and challenging. These environments require *interactive control* — the robots must run towards a flag, whose position randomly varies over time.

HumanoidFlagrun is designed to teach the robot to slow down and turn. The goal is to run towards the flag, whose position varies randomly.

HumanoidFlagrunHarder in addition allows the robot to fall and gives it time to get back on foot. It also starts each episode upright or laying on the ground, and the robot is constantly bombarded by white cubes to push it off its trajectory.

We ship trained policies for both

[HumanoidFlagrun(opens in a new window)](https://github.com/openai/roboschool/blob/master/agent_zoo/RoboschoolHumanoidFlagrun_v0_2017may.py) and [HumanoidFlagrunHarder(opens in a new window)](https://github.com/openai/roboschool/blob/master/agent_zoo/RoboschoolHumanoidFlagrunHarder_v0_2017may.py). The walks aren’t as fast and natural-looking as the ones we see from the regular humanoid, but these policies can recover from many situations, and they know how to steer. This policy itself is still a multilayer perceptron, which has no internal state, so we believe that in some cases the agent uses its arms to store information.

Roboschool lets you both run and train multiple agents in the same environment. We start with RoboschoolPong, with more environments to follow.

With multiplayer training, you can train the same agent playing for both parties (so it plays with itself), you can train two different agents using the same algorithm, or you can even set two different algorithms against each other.

The multi-agent setting presents some interesting challenges. If you train both players simultaneously, you’ll likely see a learning curve like the following one, obtained from a policy gradient method:

![Image11](https://images.ctfassets.net/kftzwdyauwt9/5a9e7de3-b1e0-4249-576ecca397c2/42b93e28d88911b643f26406cf52f879/image11.png?w=3840&q=90&fm=webp)

Learning curves for pong, where policies are updated with policy gradient algorithms running simultaneously.

Here’s what’s happening:

- Agent1 (green) learns it can sometimes hit a ball at the top, so it moves to the top.
- Agent2 (purple) discovers that its adversary is at the top, so it sends the ball to the bottom and overfits to other agent being away.
- Agent1 eventually discovers it can defend itself by moving to the bottom, but now always stay at the bottom, because Agent2 always sends ball to the bottom.

That way, the policies oscillated, and neither agent learned anything useful after hours of training. As in generative adversarial networks, learning in an adversarial setting is tricky, but we think it’s an interesting research problem because this interplay can lead to sophisticated strategies even in simple environments, and it can provide a natural curriculum.

There’s been a lot of work by the community to create [environments for OpenAI Gym(opens in a new window)](https://github.com/openai/gym/blob/master/docs/environments.md), some of which are based on open-source physics simulators. In one recent project, researchers created a [fork of OpenAI Gym(opens in a new window)](https://github.com/DartEnv/dart-env) that replaced MuJoCo by the open-source physics simulator [DART(opens in a new window)](https://dartsim.github.io/). They [showed(opens in a new window)](https://github.com/DartEnv/dart-env/wiki/OpenAI-Gym-Environments) that policies can even be transferred between the two physics simulators, MuJoCo and DART.

## Related articles

[View all](https://openai.com/news/)
