# 차선 인식 데이터셋

<br>

나의 경우 TuSimple 데이터셋을 사용했고, pytorch를 사용하므로 `Ultra Fast Structure-aware Deep Lane Detection` 논문을 참고하여 제작했다. 차선 인식 데이터셋에 대한 자세한 내용은 [이 파일](https://github.com/dkssud8150/lane_detect_yolov3/blob/master/datasets/compare_dataset.md)을 참고하길 바란다.

in my case, i use the TuSimple dataset, and pytorch. so i refer to the paper `Ultra Fast Structure-aware Deep Lane Detection`. if you need to more details lane detection dataset or comparing many lane detection dataset, you have to see [this file](https://github.com/dkssud8150/lane_detect_yolov3/blob/master/datasets/compare_dataset.md).

<br>

## 1. dataset download

```bash
sh install_data.sh
```

in this file, there are the installing codes in the TuSimple [repo](https://github.com/TuSimple/tusimple-benchmark/issues/3). you can download the train_set.zip, test_set.zip

<br>

in TuSimple, the segmentation annotations is not provided, so if you need to generate segmentation, you have to execute this code

```bash
python scripts/convert_tusimple.py --root $TUSIMPLEROOT
# this will generate segmentations and two list files: train_gt.txt and test.txt
```
