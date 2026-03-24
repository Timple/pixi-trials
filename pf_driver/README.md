When compiling with `-DCMAKE_CXX_FLAGS=-O2` the `pf_driver` packages errors on:

```
In file included from /home/tim/ros/uvee/system/.pixi/envs/default/src/gtest_vendor/src/gtest-all.cc:49:
/home/tim/ros/uvee/system/.pixi/envs/default/src/gtest_vendor/./src/gtest.cc:2720:1: error: no declaration matches 'testing::TestInfo::TestInfo(const std::string&, const std::string&, const char*, const char*, testing::internal::CodeLocation, testing::internal::TypeId, testing::internal::TestFactoryBase*)'
 2720 | TestInfo::TestInfo(const std::string& a_test_suite_name,
      | ^~~~~~~~
```

These settings do work on ubuntu 24.04 with ROS2 Jazzy & Kilted without pixi.

Try with

```
docker build .
```
