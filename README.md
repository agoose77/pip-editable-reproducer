# demo

Installing this repo using `pip install -e .` does not install `numpy` as a dependency. However, the wheel that `pip` builds does include this in the metadata, suggesting that pip is ignoring the dependencies of the editable wheel.

If you disable build isolation:
```bash
pip install -e . -vvv --no-build-isolation
```

then pip _does_ pick up these editable dependencies.
