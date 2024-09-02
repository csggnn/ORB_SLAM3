- I had to change c++11 -> C++14 in order to build.
- For Sophus, I had to disable -Werror
- Activate visualization in mono_tum_vi.cc at line:
    `ORB_SLAM3::System SLAM(argv[1],argv[2],ORB_SLAM3::System::MONOCULAR,true /* visualization was set to false */ , 0, file_name);`
- Build using OpenCV from apt (the one I built was missing libgtk). I had to manually rebuild `libDBoW2.so` which would otherwise look for opencv4.10 while linux gives me 4.6
- Test run from `~/Projects/ORB_SLAM3/Examples/Monocular`: `./mono_tum_vi  ../../Vocabulary/ORBvoc.txt TUM-VI.yaml ../../data/tum_vi/dataset-magistrale3_512_16/mav0/cam0/data/ TUM_TimeStamps/dataset-magistrale3_512.txt`