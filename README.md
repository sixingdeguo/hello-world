  ERROR: Command errored out with exit status 1:
   command: /usr/local/bin/python3.10 -u -c 'import io, os, sys, setuptools, tokenize; sys.argv[0] = '"'"'/tmp/pip-install-xexdh0bm/gym_de0b719667d24dc9bdd928e9a08e48be/setup.py'"'"'; __file__='"'"'/tmp/pip-install-xexdh0bm/gym_de0b719667d24dc9bdd928e9a08e48be/setup.py'"'"';f = getattr(tokenize, '"'"'open'"'"', open)(__file__) if os.path.exists(__file__) else io.StringIO('"'"'from setuptools import setup; setup()'"'"');code = f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' bdist_wheel -d /tmp/pip-wheel-xegab7wb
       cwd: /tmp/pip-install-xexdh0bm/gym_de0b719667d24dc9bdd928e9a08e48be/
  Complete output (480 lines):
  running bdist_wheel
  running build
  running build_py
  creating build
  creating build/lib
  creating build/lib/gym
  copying gym/logger.py -> build/lib/gym
  copying gym/version.py -> build/lib/gym
  copying gym/core.py -> build/lib/gym
  copying gym/error.py -> build/lib/gym
  copying gym/__init__.py -> build/lib/gym
  creating build/lib/gym/utils
  copying gym/utils/atomic_write.py -> build/lib/gym/utils
  copying gym/utils/play.py -> build/lib/gym/utils
  copying gym/utils/ezpickle.py -> build/lib/gym/utils
  copying gym/utils/closer.py -> build/lib/gym/utils
  copying gym/utils/colorize.py -> build/lib/gym/utils
  copying gym/utils/seeding.py -> build/lib/gym/utils
  copying gym/utils/json_utils.py -> build/lib/gym/utils
  copying gym/utils/env_checker.py -> build/lib/gym/utils
  copying gym/utils/__init__.py -> build/lib/gym/utils
  creating build/lib/gym/spaces
  copying gym/spaces/discrete.py -> build/lib/gym/spaces
  copying gym/spaces/tuple.py -> build/lib/gym/spaces
  copying gym/spaces/dict.py -> build/lib/gym/spaces
  copying gym/spaces/box.py -> build/lib/gym/spaces
  copying gym/spaces/utils.py -> build/lib/gym/spaces
  copying gym/spaces/__init__.py -> build/lib/gym/spaces
  copying gym/spaces/space.py -> build/lib/gym/spaces
  copying gym/spaces/multi_discrete.py -> build/lib/gym/spaces
  copying gym/spaces/multi_binary.py -> build/lib/gym/spaces
  creating build/lib/gym/vector
  copying gym/vector/async_vector_env.py -> build/lib/gym/vector
  copying gym/vector/vector_env.py -> build/lib/gym/vector
  copying gym/vector/sync_vector_env.py -> build/lib/gym/vector
  copying gym/vector/__init__.py -> build/lib/gym/vector
  creating build/lib/gym/envs
  copying gym/envs/registration.py -> build/lib/gym/envs
  copying gym/envs/__init__.py -> build/lib/gym/envs
  creating build/lib/gym/wrappers
  copying gym/wrappers/resize_observation.py -> build/lib/gym/wrappers
  copying gym/wrappers/record_video.py -> build/lib/gym/wrappers
  copying gym/wrappers/frame_stack.py -> build/lib/gym/wrappers
  copying gym/wrappers/pixel_observation.py -> build/lib/gym/wrappers
  copying gym/wrappers/filter_observation.py -> build/lib/gym/wrappers
  copying gym/wrappers/gray_scale_observation.py -> build/lib/gym/wrappers
  copying gym/wrappers/transform_observation.py -> build/lib/gym/wrappers
  copying gym/wrappers/normalize.py -> build/lib/gym/wrappers
  copying gym/wrappers/time_aware_observation.py -> build/lib/gym/wrappers
  copying gym/wrappers/record_episode_statistics.py -> build/lib/gym/wrappers
  copying gym/wrappers/order_enforcing.py -> build/lib/gym/wrappers
  copying gym/wrappers/time_limit.py -> build/lib/gym/wrappers
  copying gym/wrappers/atari_preprocessing.py -> build/lib/gym/wrappers
  copying gym/wrappers/clip_action.py -> build/lib/gym/wrappers
  copying gym/wrappers/transform_reward.py -> build/lib/gym/wrappers
  copying gym/wrappers/monitor.py -> build/lib/gym/wrappers
  copying gym/wrappers/rescale_action.py -> build/lib/gym/wrappers
  copying gym/wrappers/__init__.py -> build/lib/gym/wrappers
  copying gym/wrappers/flatten_observation.py -> build/lib/gym/wrappers
  creating build/lib/gym/vector/utils
  copying gym/vector/utils/spaces.py -> build/lib/gym/vector/utils
  copying gym/vector/utils/shared_memory.py -> build/lib/gym/vector/utils
  copying gym/vector/utils/misc.py -> build/lib/gym/vector/utils
  copying gym/vector/utils/numpy_utils.py -> build/lib/gym/vector/utils
  copying gym/vector/utils/__init__.py -> build/lib/gym/vector/utils
  creating build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/humanoid_v3.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/mujoco_env.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/hopper.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/ant_v3.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/inverted_double_pendulum.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/walker2d.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/striker.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/ant.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/humanoid.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/pusher.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/swimmer.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/hopper_v3.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/walker2d_v3.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/half_cheetah.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/reacher.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/humanoidstandup.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/thrower.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/__init__.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/inverted_pendulum.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/half_cheetah_v3.py -> build/lib/gym/envs/mujoco
  copying gym/envs/mujoco/swimmer_v3.py -> build/lib/gym/envs/mujoco
  creating build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/mountain_car.py -> build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/pendulum.py -> build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/cartpole.py -> build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/continuous_mountain_car.py -> build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/acrobot.py -> build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/rendering.py -> build/lib/gym/envs/classic_control
  copying gym/envs/classic_control/__init__.py -> build/lib/gym/envs/classic_control
  creating build/lib/gym/envs/toy_text
  copying gym/envs/toy_text/taxi.py -> build/lib/gym/envs/toy_text
  copying gym/envs/toy_text/discrete.py -> build/lib/gym/envs/toy_text
  copying gym/envs/toy_text/cliffwalking.py -> build/lib/gym/envs/toy_text
  copying gym/envs/toy_text/frozen_lake.py -> build/lib/gym/envs/toy_text
  copying gym/envs/toy_text/blackjack.py -> build/lib/gym/envs/toy_text
  copying gym/envs/toy_text/__init__.py -> build/lib/gym/envs/toy_text
  creating build/lib/gym/envs/unittest
  copying gym/envs/unittest/memorize_digits.py -> build/lib/gym/envs/unittest
  copying gym/envs/unittest/cube_crash.py -> build/lib/gym/envs/unittest
  copying gym/envs/unittest/__init__.py -> build/lib/gym/envs/unittest
  creating build/lib/gym/envs/robotics
  copying gym/envs/robotics/rotations.py -> build/lib/gym/envs/robotics
  copying gym/envs/robotics/hand_env.py -> build/lib/gym/envs/robotics
  copying gym/envs/robotics/fetch_env.py -> build/lib/gym/envs/robotics
  copying gym/envs/robotics/robot_env.py -> build/lib/gym/envs/robotics
  copying gym/envs/robotics/utils.py -> build/lib/gym/envs/robotics
  copying gym/envs/robotics/__init__.py -> build/lib/gym/envs/robotics
  creating build/lib/gym/envs/box2d
  copying gym/envs/box2d/lunar_lander.py -> build/lib/gym/envs/box2d
  copying gym/envs/box2d/car_racing.py -> build/lib/gym/envs/box2d
  copying gym/envs/box2d/bipedal_walker.py -> build/lib/gym/envs/box2d
  copying gym/envs/box2d/car_dynamics.py -> build/lib/gym/envs/box2d
  copying gym/envs/box2d/__init__.py -> build/lib/gym/envs/box2d
  creating build/lib/gym/envs/robotics/hand
  copying gym/envs/robotics/hand/manipulate.py -> build/lib/gym/envs/robotics/hand
  copying gym/envs/robotics/hand/reach.py -> build/lib/gym/envs/robotics/hand
  copying gym/envs/robotics/hand/manipulate_touch_sensors.py -> build/lib/gym/envs/robotics/hand
  copying gym/envs/robotics/hand/__init__.py -> build/lib/gym/envs/robotics/hand
  creating build/lib/gym/envs/robotics/fetch
  copying gym/envs/robotics/fetch/push.py -> build/lib/gym/envs/robotics/fetch
  copying gym/envs/robotics/fetch/slide.py -> build/lib/gym/envs/robotics/fetch
  copying gym/envs/robotics/fetch/reach.py -> build/lib/gym/envs/robotics/fetch
  copying gym/envs/robotics/fetch/__init__.py -> build/lib/gym/envs/robotics/fetch
  copying gym/envs/robotics/fetch/pick_and_place.py -> build/lib/gym/envs/robotics/fetch
  creating build/lib/gym/wrappers/monitoring
  copying gym/wrappers/monitoring/video_recorder.py -> build/lib/gym/wrappers/monitoring
  copying gym/wrappers/monitoring/stats_recorder.py -> build/lib/gym/wrappers/monitoring
  copying gym/wrappers/monitoring/__init__.py -> build/lib/gym/wrappers/monitoring
  creating build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/striker.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/half_cheetah.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/humanoidstandup.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/inverted_double_pendulum.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/swimmer.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/humanoid.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/pusher.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/inverted_pendulum.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/walker2d.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/ant.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/reacher.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/thrower.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/point.xml -> build/lib/gym/envs/mujoco/assets
  copying gym/envs/mujoco/assets/hopper.xml -> build/lib/gym/envs/mujoco/assets
  creating build/lib/gym/envs/classic_control/assets
  copying gym/envs/classic_control/assets/clockwise.png -> build/lib/gym/envs/classic_control/assets
  creating build/lib/gym/envs/robotics/assets
  copying gym/envs/robotics/assets/LICENSE.md -> build/lib/gym/envs/robotics/assets
  creating build/lib/gym/envs/robotics/assets/fetch
  copying gym/envs/robotics/assets/fetch/reach.xml -> build/lib/gym/envs/robotics/assets/fetch
  copying gym/envs/robotics/assets/fetch/shared.xml -> build/lib/gym/envs/robotics/assets/fetch
  copying gym/envs/robotics/assets/fetch/push.xml -> build/lib/gym/envs/robotics/assets/fetch
  copying gym/envs/robotics/assets/fetch/slide.xml -> build/lib/gym/envs/robotics/assets/fetch
  copying gym/envs/robotics/assets/fetch/robot.xml -> build/lib/gym/envs/robotics/assets/fetch
  copying gym/envs/robotics/assets/fetch/pick_and_place.xml -> build/lib/gym/envs/robotics/assets/fetch
  creating build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/manipulate_egg.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/manipulate_pen.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/shared_asset.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/manipulate_block.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/reach.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/shared.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/shared_touch_sensors_92.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/manipulate_block_touch_sensors.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/manipulate_egg_touch_sensors.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/manipulate_pen_touch_sensors.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/robot.xml -> build/lib/gym/envs/robotics/assets/hand
  copying gym/envs/robotics/assets/hand/robot_touch_sensors_92.xml -> build/lib/gym/envs/robotics/assets/hand
  creating build/lib/gym/envs/robotics/assets/stls
  creating build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/elbow_flex_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/base_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/head_tilt_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/r_wheel_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/gripper_link.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/torso_fixed_link.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/shoulder_pan_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/wrist_flex_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/torso_lift_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/shoulder_lift_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/wrist_roll_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/head_pan_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/l_wheel_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/bellows_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/estop_link.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/upperarm_roll_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/forearm_roll_link_collision.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  copying gym/envs/robotics/assets/stls/fetch/laser_link.stl -> build/lib/gym/envs/robotics/assets/stls/fetch
  creating build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/forearm_electric.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/knuckle.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/forearm_electric_cvx.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/F2.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/F3.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/F1.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/TH1_z.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/palm.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/lfmetacarpal.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/TH2_z.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/TH3_z.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  copying gym/envs/robotics/assets/stls/hand/wrist.stl -> build/lib/gym/envs/robotics/assets/stls/hand
  creating build/lib/gym/envs/robotics/assets/textures
  copying gym/envs/robotics/assets/textures/block.png -> build/lib/gym/envs/robotics/assets/textures
  copying gym/envs/robotics/assets/textures/block_hidden.png -> build/lib/gym/envs/robotics/assets/textures
  /usr/local/lib/python3.10/site-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
    warnings.warn(
  installing to build/bdist.linux-x86_64/wheel
  running install
  running install_lib
  creating build/bdist.linux-x86_64
  creating build/bdist.linux-x86_64/wheel
  creating build/bdist.linux-x86_64/wheel/gym
  creating build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/atomic_write.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/play.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/ezpickle.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/closer.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/colorize.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/seeding.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/json_utils.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/env_checker.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/utils/__init__.py -> build/bdist.linux-x86_64/wheel/gym/utils
  copying build/lib/gym/logger.py -> build/bdist.linux-x86_64/wheel/gym
  creating build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/discrete.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/tuple.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/dict.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/box.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/utils.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/__init__.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/space.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/multi_discrete.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/spaces/multi_binary.py -> build/bdist.linux-x86_64/wheel/gym/spaces
  copying build/lib/gym/version.py -> build/bdist.linux-x86_64/wheel/gym
  creating build/bdist.linux-x86_64/wheel/gym/vector
  copying build/lib/gym/vector/async_vector_env.py -> build/bdist.linux-x86_64/wheel/gym/vector
  copying build/lib/gym/vector/vector_env.py -> build/bdist.linux-x86_64/wheel/gym/vector
  creating build/bdist.linux-x86_64/wheel/gym/vector/utils
  copying build/lib/gym/vector/utils/spaces.py -> build/bdist.linux-x86_64/wheel/gym/vector/utils
  copying build/lib/gym/vector/utils/shared_memory.py -> build/bdist.linux-x86_64/wheel/gym/vector/utils
  copying build/lib/gym/vector/utils/misc.py -> build/bdist.linux-x86_64/wheel/gym/vector/utils
  copying build/lib/gym/vector/utils/numpy_utils.py -> build/bdist.linux-x86_64/wheel/gym/vector/utils
  copying build/lib/gym/vector/utils/__init__.py -> build/bdist.linux-x86_64/wheel/gym/vector/utils
  copying build/lib/gym/vector/sync_vector_env.py -> build/bdist.linux-x86_64/wheel/gym/vector
  copying build/lib/gym/vector/__init__.py -> build/bdist.linux-x86_64/wheel/gym/vector
  creating build/bdist.linux-x86_64/wheel/gym/envs
  creating build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/humanoid_v3.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/mujoco_env.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/hopper.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/ant_v3.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/inverted_double_pendulum.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/walker2d.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/striker.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/ant.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  creating build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/striker.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/half_cheetah.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/humanoidstandup.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/inverted_double_pendulum.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/swimmer.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/humanoid.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/pusher.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/inverted_pendulum.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/walker2d.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/ant.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/reacher.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/thrower.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/point.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/assets/hopper.xml -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco/assets
  copying build/lib/gym/envs/mujoco/humanoid.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/pusher.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/swimmer.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/hopper_v3.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/walker2d_v3.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/half_cheetah.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/reacher.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/humanoidstandup.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/thrower.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/inverted_pendulum.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/half_cheetah_v3.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  copying build/lib/gym/envs/mujoco/swimmer_v3.py -> build/bdist.linux-x86_64/wheel/gym/envs/mujoco
  creating build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  copying build/lib/gym/envs/classic_control/mountain_car.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  creating build/bdist.linux-x86_64/wheel/gym/envs/classic_control/assets
  copying build/lib/gym/envs/classic_control/assets/clockwise.png -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control/assets
  copying build/lib/gym/envs/classic_control/pendulum.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  copying build/lib/gym/envs/classic_control/cartpole.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  copying build/lib/gym/envs/classic_control/continuous_mountain_car.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  copying build/lib/gym/envs/classic_control/acrobot.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  copying build/lib/gym/envs/classic_control/rendering.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  copying build/lib/gym/envs/classic_control/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/classic_control
  creating build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/toy_text/taxi.py -> build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/toy_text/discrete.py -> build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/toy_text/cliffwalking.py -> build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/toy_text/frozen_lake.py -> build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/toy_text/blackjack.py -> build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/toy_text/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/toy_text
  copying build/lib/gym/envs/registration.py -> build/bdist.linux-x86_64/wheel/gym/envs
  creating build/bdist.linux-x86_64/wheel/gym/envs/unittest
  copying build/lib/gym/envs/unittest/memorize_digits.py -> build/bdist.linux-x86_64/wheel/gym/envs/unittest
  copying build/lib/gym/envs/unittest/cube_crash.py -> build/bdist.linux-x86_64/wheel/gym/envs/unittest
  copying build/lib/gym/envs/unittest/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/unittest
  copying build/lib/gym/envs/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics
  copying build/lib/gym/envs/robotics/rotations.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets
  copying build/lib/gym/envs/robotics/assets/LICENSE.md -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/manipulate_egg.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/manipulate_pen.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/shared_asset.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/manipulate_block.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/reach.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/shared.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/shared_touch_sensors_92.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/manipulate_block_touch_sensors.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/manipulate_egg_touch_sensors.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/manipulate_pen_touch_sensors.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/robot.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  copying build/lib/gym/envs/robotics/assets/hand/robot_touch_sensors_92.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/hand
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/forearm_electric.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/knuckle.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/forearm_electric_cvx.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/F2.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/F3.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/F1.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/TH1_z.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/palm.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/lfmetacarpal.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/TH2_z.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/TH3_z.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  copying build/lib/gym/envs/robotics/assets/stls/hand/wrist.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/hand
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/elbow_flex_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/base_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/head_tilt_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/r_wheel_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/gripper_link.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/torso_fixed_link.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/shoulder_pan_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/wrist_flex_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/torso_lift_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/shoulder_lift_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/wrist_roll_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/head_pan_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/l_wheel_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/bellows_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/estop_link.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/upperarm_roll_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/forearm_roll_link_collision.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  copying build/lib/gym/envs/robotics/assets/stls/fetch/laser_link.stl -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/stls/fetch
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/textures
  copying build/lib/gym/envs/robotics/assets/textures/block.png -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/textures
  copying build/lib/gym/envs/robotics/assets/textures/block_hidden.png -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/textures
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/assets/fetch/reach.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/assets/fetch/shared.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/assets/fetch/push.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/assets/fetch/slide.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/assets/fetch/robot.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/assets/fetch/pick_and_place.xml -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/assets/fetch
  copying build/lib/gym/envs/robotics/hand_env.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics
  copying build/lib/gym/envs/robotics/fetch_env.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/hand
  copying build/lib/gym/envs/robotics/hand/manipulate.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/hand
  copying build/lib/gym/envs/robotics/hand/reach.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/hand
  copying build/lib/gym/envs/robotics/hand/manipulate_touch_sensors.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/hand
  copying build/lib/gym/envs/robotics/hand/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/hand
  copying build/lib/gym/envs/robotics/robot_env.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics
  copying build/lib/gym/envs/robotics/utils.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics
  creating build/bdist.linux-x86_64/wheel/gym/envs/robotics/fetch
  copying build/lib/gym/envs/robotics/fetch/push.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/fetch
  copying build/lib/gym/envs/robotics/fetch/slide.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/fetch
  copying build/lib/gym/envs/robotics/fetch/reach.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/fetch
  copying build/lib/gym/envs/robotics/fetch/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/fetch
  copying build/lib/gym/envs/robotics/fetch/pick_and_place.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics/fetch
  copying build/lib/gym/envs/robotics/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/robotics
  creating build/bdist.linux-x86_64/wheel/gym/envs/box2d
  copying build/lib/gym/envs/box2d/lunar_lander.py -> build/bdist.linux-x86_64/wheel/gym/envs/box2d
  copying build/lib/gym/envs/box2d/car_racing.py -> build/bdist.linux-x86_64/wheel/gym/envs/box2d
  copying build/lib/gym/envs/box2d/bipedal_walker.py -> build/bdist.linux-x86_64/wheel/gym/envs/box2d
  copying build/lib/gym/envs/box2d/car_dynamics.py -> build/bdist.linux-x86_64/wheel/gym/envs/box2d
  copying build/lib/gym/envs/box2d/__init__.py -> build/bdist.linux-x86_64/wheel/gym/envs/box2d
  copying build/lib/gym/core.py -> build/bdist.linux-x86_64/wheel/gym
  copying build/lib/gym/error.py -> build/bdist.linux-x86_64/wheel/gym
  copying build/lib/gym/__init__.py -> build/bdist.linux-x86_64/wheel/gym
  creating build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/resize_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/record_video.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  creating build/bdist.linux-x86_64/wheel/gym/wrappers/monitoring
  copying build/lib/gym/wrappers/monitoring/video_recorder.py -> build/bdist.linux-x86_64/wheel/gym/wrappers/monitoring
  copying build/lib/gym/wrappers/monitoring/stats_recorder.py -> build/bdist.linux-x86_64/wheel/gym/wrappers/monitoring
  copying build/lib/gym/wrappers/monitoring/__init__.py -> build/bdist.linux-x86_64/wheel/gym/wrappers/monitoring
  copying build/lib/gym/wrappers/frame_stack.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/pixel_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/filter_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/gray_scale_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/transform_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/normalize.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/time_aware_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/record_episode_statistics.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/order_enforcing.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/time_limit.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/atari_preprocessing.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/clip_action.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/transform_reward.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/monitor.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/rescale_action.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/__init__.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  copying build/lib/gym/wrappers/flatten_observation.py -> build/bdist.linux-x86_64/wheel/gym/wrappers
  running install_egg_info
  running egg_info
  writing gym.egg-info/PKG-INFO
  writing dependency_links to gym.egg-info/dependency_links.txt
  writing requirements to gym.egg-info/requires.txt
  writing top-level names to gym.egg-info/top_level.txt
  reading manifest file 'gym.egg-info/SOURCES.txt'
  writing manifest file 'gym.egg-info/SOURCES.txt'
  Copying gym.egg-info to build/bdist.linux-x86_64/wheel/gym-0.21.0-py3.10.egg-info
  running install_scripts
  Traceback (most recent call last):
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/requirements.py", line 35, in __init__
      parsed = _parse_requirement(requirement_string)
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/_parser.py", line 64, in parse_requirement
      return _parse_requirement(Tokenizer(source, rules=DEFAULT_RULES))
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/_parser.py", line 82, in _parse_requirement
      url, specifier, marker = _parse_requirement_details(tokenizer)
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/_parser.py", line 126, in _parse_requirement_details
      marker = _parse_requirement_marker(
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/_parser.py", line 147, in _parse_requirement_marker
      tokenizer.raise_syntax_error(
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/_tokenizer.py", line 165, in raise_syntax_error
      raise ParserSyntaxError(
  wheel.vendored.packaging._tokenizer.ParserSyntaxError: Expected end or semicolon (after version specifier)
      opencv-python>=3.
                   ~~~^
  
  The above exception was the direct cause of the following exception:
  
  Traceback (most recent call last):
    File "<string>", line 1, in <module>
    File "/tmp/pip-install-xexdh0bm/gym_de0b719667d24dc9bdd928e9a08e48be/setup.py", line 39, in <module>
      setup(
    File "/usr/local/lib/python3.10/site-packages/setuptools/__init__.py", line 87, in setup
      return distutils.core.setup(**attrs)
    File "/usr/local/lib/python3.10/site-packages/setuptools/_distutils/core.py", line 185, in setup
      return run_commands(dist)
    File "/usr/local/lib/python3.10/site-packages/setuptools/_distutils/core.py", line 201, in run_commands
      dist.run_commands()
    File "/usr/local/lib/python3.10/site-packages/setuptools/_distutils/dist.py", line 968, in run_commands
      self.run_command(cmd)
    File "/usr/local/lib/python3.10/site-packages/setuptools/dist.py", line 1217, in run_command
      super().run_command(command)
    File "/usr/local/lib/python3.10/site-packages/setuptools/_distutils/dist.py", line 987, in run_command
      cmd_obj.run()
    File "/usr/local/lib/python3.10/site-packages/wheel/bdist_wheel.py", line 420, in run
      self.egg2dist(self.egginfo_dir, distinfo_dir)
    File "/usr/local/lib/python3.10/site-packages/wheel/bdist_wheel.py", line 561, in egg2dist
      pkg_info = pkginfo_to_metadata(egginfo_path, pkginfo_path)
    File "/usr/local/lib/python3.10/site-packages/wheel/metadata.py", line 161, in pkginfo_to_metadata
      for key, value in generate_requirements({extra: reqs}):
    File "/usr/local/lib/python3.10/site-packages/wheel/metadata.py", line 139, in generate_requirements
      for new_req in convert_requirements(depends):
    File "/usr/local/lib/python3.10/site-packages/wheel/metadata.py", line 104, in convert_requirements
      parsed_requirement = Requirement(req)
    File "/usr/local/lib/python3.10/site-packages/wheel/vendored/packaging/requirements.py", line 37, in __init__
      raise InvalidRequirement(str(e)) from e
  wheel.vendored.packaging.requirements.InvalidRequirement: Expected end or semicolon (after version specifier)
      opencv-python>=3.
                   ~~~^
  ----------------------------------------
  ERROR: Failed building wheel for gym
