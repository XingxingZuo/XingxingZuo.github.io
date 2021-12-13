- If you change anything in `_config.yml`, you have to rebuild the website again after that (e.g., if you are running `bundle exec jekyll serve`, you have to kill it and re-run again). [Directory is not right after changing _config.yml](https://github.com/alshedivat/al-folio/issues/318)

  > ```shell
  > $ bundle install
  > $ bundle exec jekyll serve
  > ```

- Please refer to https://github.com/yiyiliao/yiyiliao.github.io/commits/master?before=e5e91d551e314871ec9db0e085c7ea49b6e73134+35&branch=master for modifying it.

https://github.com/eaplatanios/eaplatanios.github.io

https://github.com/otiliastr/otiliastr.github.io



```

# {: #publications}
# ## __publications__

# {% for y in page.years %}
#   {% bibliography -f papers -q @*[year={{y}}]* %}
# {% endfor %} 
```



```
@InProceedings{Zuo2019IROS,
  Title                    = {LIC-Fusion: LiDAR-Inertial-Camera Odometry},
  Author                   = {Zuo, Xingxing and Geneva, Patrick and Lee, Woosik and Liu, Yong and Huang, Guoquan},
  Booktitle                = {Proc. IEEE/RSJ International Conference on Intelligent Robots and Systems},
    year={2019},
  pages={5848-5854},
  doi={10.1109/IROS40897.2019.8967746},
  Address                  = {Macau, China}
}

@InProceedings{Zuo2019ISRR,
  Title                    = {Visual-Inertial Localization for Skid-Steering Robots with Kinematic Constraints},
  Author                   = {Zuo, Xingxing and Zhang, Mingming and Chen, Yiming and Liu, Yong and Huang, Guoquan and Li, Mingyang},
  Booktitle                = {International Symposium on Robotics Research (ISRR)},
  Year                     = {2019},
    Address                  = {Hanoi, Vietnam}
}

@InProceedings{Zuo2020IROS,
  Title                    = {LIC-Fusion 2.0: LiDAR-Inertial-Camera Odometry with Sliding-Window Plane-Feature Tracking},
  author={Zuo, Xingxing and Yang, Yulin and Geneva, Patrick and Lv, Jiajun and Liu, Yong and Huang, Guoquan and Pollefeys, Marc},
  Booktitle                = {Proc. IEEE/RSJ International Conference on Intelligent Robots and Systems},
  year={2020},
  pages={5112-5119},
  Address                  = {Las Vegas, NV, USA},
  url={https://arxiv.org/pdf/2008.07196}
}


@article{zuo2020multimodal,
  title={Multimodal localization: Stereo over LiDAR map},
  author={Zuo, Xingxing and Ye, Wenlong and Yang, Yulin and Zheng, Renjie and Vidal-Calleja, Teresa and Huang, Guoquan and Liu, Yong},
  journal={Journal of Field Robotics},
  volume={37},
  number={6},
  pages={1003--1026},
  year={2020},
  publisher={Wiley Online Library}
}


@article{zhang2021pose,
  title={Pose Estimation for Ground Robots: On Manifold Representation, Integration, Reparameterization, and Optimization},
  author={Zhang, Mingming and Zuo, Xingxing and Chen, Yiming and Liu, Yong and Li, Mingyang},
  journal={IEEE Transactions on Robotics},
  year={2021},
  volume={37},
  number={4},
  pages={1081-1099},
  publisher={IEEE}
}
```

