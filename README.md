## Parameter scenarios

| Param file | Robot | Sim/Real | World | Sensors | Maps Managers | Localizer | Planner | Controller |
|-----------|-------|----------|-------|---------|---------------|-----------|---------|------------|
| [Test1](robots_params/dummy.params.yaml) | Kobuki | None | None | None | Dummy | Dummy | Dummy | Dummy |
| [Test2](robots_params/dummy.sensor.params.yaml) | Kobuki | Sim | House | Laser | Simple | AMCL/Simple | Dummy | Dummy |
| [Test3](robots_params/simple.params.yaml) | Kobuki | Sim | House | Laser | Simple | AMCL/Simple | A*/Simple | Simple |
| [Test4](robots_params/costmap.serest.params.yaml) | Kobuki | Sim | House | Laser | Costmap (obstacles + inflation) | AMCL/Costmap | A*/Costmap | Serest |
| [Test5](robots_params/costmap.mppi.routed.params.yaml) | Kobuki | Sim | House | Laser | Costmap (obstacles + inflation) + Routes | AMCL/Costmap | A*/Costmap | MPPI |
| [Test6](robots_params/costmap.mpc.params.yaml) | Kobuki | Sim | House | Laser | Costmap (obstacles + inflation) | AMCL/Costmap | A*/Costmap | MPC  + Collision |
| [Test7](robots_params/summit_gridmap_ls_params.yaml) | Summit XL | Sim | URJC Dig | Laser 3D | NavMap | LidarSlam | A*/Gridmap | MPC |
| [Test8](robots_params/bonxai.amcl.params.urjc) | Summit XL | Sim | URJC Dig | Laser 3D | Bonxai + NavMap (obstacles + inflation) | AMCL | A*/Gridmap | MPC |

## Install

First get all the required dependencies:
```
rosdep install --from-paths src --ignore-src -r -y
```
