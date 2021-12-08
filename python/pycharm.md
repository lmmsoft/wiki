# pycharm

## pytest 在 pycharm 里面无法 debug
- 因为 pytest.ini 里有 --cov 参数
- Hack方法: 
  - add --no-cov on the Additional Arguments on the Run/Debug Configurations.
  - Update Templates -> Python tests -> pytest, so every new test gets this configuration.
- 参考文章
  - https://newbedev.com/unable-to-debug-in-pycharm-with-pytest
  - https://stackoverflow.com/questions/40718760/unable-to-debug-in-pycharm-with-pytest
