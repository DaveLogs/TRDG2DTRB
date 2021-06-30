# TextRecognitionDataGenerator to Deep-Text-Recognition-Benchmark



Convert TextRecognitionDataGenerator's result data to Deep-Text-Recognition-Benchmark's input data.



## Reference projects

- [TextRecognitionDataGenerator](https://github.com/Belval/TextRecognitionDataGenerator): A synthetic data generator for text recognition.
- [deep-text-recognition-benchmark](https://github.com/clovaai/deep-text-recognition-benchmark): Text recognition (optical character recognition) with deep learning methods.



## Usage example

```bash
(venv) $ python3 convert.py \
	--input_path ./input \
  	--output_path ./output
```



## Data Structures

The structure of data folder as below.

* Input: result of [TextRecognitionDataGenerator](https://github.com/Belval/TextRecognitionDataGenerator) project.

```
/input
#   [gt]_[idx].[ext]
├── abcd_00001.jpg
├── efgh_00002.jpg
├── ijkl_00003.jpg
└── ...
```



* Output: for use in [deep-text-recognition-benchmark](https://github.com/clovaai/deep-text-recognition-benchmark) project.

```
/output
├── gt.txt
└── /images
    #  	image_[idx].[ext]
    ├── image_00001.png
    ├── image_00002.png
    ├── image_00003.png
    └── ...
```



## Ground truth file structure

* gt.txt

```
# {filename}\t{label}\n
  images/image_00001.png	abcd
  images/image_00002.png	efgh
  images/image_00003.png	ijkl
  ...
```

