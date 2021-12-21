# chowdsp_juce_dsp

A copy of the [JUCE DSP module](https://github.com/juce-framework/JUCE/tree/master/modules/juce_dsp)
with a couple modifications:
- Implemented SIMD operations for NEON double-precision

If you are using this code, please make sure to abide by the [JUCE licensing agreement](https://github.com/juce-framework/JUCE/blob/master/LICENSE.md)

### Compatibility with `juce_dsp`

All of the files in this repo are compatible with the equivalent
files in `juce_dsp`, except for:
- native/juce_neon_SIMDNativeOps.*

### Updating this module

Sometimes, it will be necessary to update this module to stay in-sync
with changes to the rest of JUCE. The process for updating should be
as follows:
```bash
# switch to juce branch
git checkout juce

# copy from mainline JUCE
cp -R path/to/juce_dsp/* .

# commit to juce branch
git commit -am "Update to JUCE version x.x.x"

# push to juce branch
git push

# switch to main branch
git checkout main

# rebase from juce branch
git rebase juce

# push to main
git push
```
