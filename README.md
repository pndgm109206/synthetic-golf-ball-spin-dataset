# synthetic-golf-ball-spin-dataset

This dataset contains synthetic golf-ball image sequences and associated motion
metadata for quantitative spin-estimation research. The sequences were rendered
in Blender using shot and timing conditions derived from a vision sensor.

## Dataset contents

| Archive | Surface pattern | Shots | Frames per shot |
| --- | --- | ---: | ---: |
| `default_logo.zip` | Default logo | 109 | 8 |
| `gtsn_test_logo.zip` | GTSN_TEST logo | 109 | 8 |
| `four_dot_cluster.zip` | Four-dot cluster mark | 109 | 8 |
| `uniform_dot.zip` | Uniform dot mark | 109 | 8 |

The four-dot cluster archive contains the spherical-circle, 1.25-spacing dataset
used for the reported experiments. The uniform-dot archive contains the original
uniform-dot dataset used for those experiments.

Each shot includes:

- `images_1280x1024/`: eight full-resolution rendered frames.
- `images_416x300/`: eight cropped input frames.
- `metadata.json`: per-frame timestamps, ball positions, rotations, projected
  centers and bounding boxes, plus camera, crop and motion information where
  present in the source metadata.

The quaternion fields use `wxyz` component order. The coordinate conventions
and units are recorded in the metadata where available. Spin and motion values
describe the configured synthetic scene; they should not be interpreted as
independent measurements of the rendered images. The images are synthetic,
not photographs.

Each archive is organized as `<pattern>/<club>/<shot>/`. The shot identifiers
are retained from the source dataset. Source computer paths, sensor packet
metadata, full sensor output and experiment logs are not included.

## Integrity

The files are available from the [dataset release](https://github.com/pndgm109206/synthetic-golf-ball-spin-dataset/releases/tag/dataset-v1.0).
See `SHA256SUMS.txt` in the release to verify the archives.

## Citation and terms

The dataset is associated with the paper titled "Spherical Image Registration
for Unmarked Golf Ball Spin Estimation and Construction of a Synthetic
Ground-Truth Dataset". Publication details will be added when available.

No dataset license or specific reuse terms have been specified. Please contact
the dataset authors about reuse, including reuse of the included logo imagery.
