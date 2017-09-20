# Kaldi Docker Images

The requirements for [Kaldi](http://kaldi-asr.org/) are a little complicated and
not very portable, so I made these so anyone can get up and running quickly.

### Shared vs. Static

Kaldi can be built with either static (default) or shared libraries [see
breakdown](http://kaldi-asr.org/doc/build_setup.html). As such, there are
two available base images to work from:

- `jbender/kaldi-static` which uses static libraries and is ~7.7 GB
- `jbender/kaldi-shared` which uses shared libraries and is only ~3.6 GB
