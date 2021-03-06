# rmf_test_scenarios
Launch files to test fleet adapters with various requests
Clone this repo into the workspace and build

Note: RAM usage seems to spike during tough negotiations.

## DP2 world
checkout `develop` branch of `sharp-rmf/rmf_dp2`
```bash
ros2 launch dp2 sim.xml
```

## Office and Airport
checkout `master` branch of `rmf_demos` 

Office
```
ros2 launch demos office.launch.xml
```

Airport
```
ros2 launch demos airport_terminal.launch.xml
ros2 run demos airport_terminal_spawn_robots.sh
```

# Scenarios
To launch a scenario,
```
ros2 launch scenarios office_conflict1.launch.xml
```
Note: For `office_delivery` scenario, the tester is required to manually re-run the launch file after each successful completion. 

Note: To make the airport scenarios run smoother, delete all the model listings under `models:` tag inside `airport_terminal.building.yaml`. Then rebuild `rmf_demo_maps` package.
