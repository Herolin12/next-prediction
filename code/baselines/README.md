## Future Prediction additional baselines


constant velocity baseline:

1. velocity the same as the last observation timestep
```
$ python code/baselines/constant_velocity.py actev_preprocess 1 --is_actev
```

2. velocity the same as the mean of all observation
```
$ python code/baselines/constant_velocity.py actev_preprocess 2 --is_actev
```

3. ETH/UCY constant velocity with our trajectory data
```
$ for dataset in {eth,hotel,univ,zara1,zara2};do python \
code/baselines/constant_velocity.py preprocess_${dataset} 2 \
--scene_h 51 --scene_w 64;done
```

ActEV world coordinates:
```
python code/baselines/img2world_traj_actev.py traj_2.5fps/ \
actev_homography traj_2.5fps_world/
```
