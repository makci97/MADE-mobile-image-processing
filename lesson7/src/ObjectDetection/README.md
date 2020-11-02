Please, review [TensorFlow instruction](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/running_on_mobile_tf2.md).
Example (Tensorflow 1.x!!!)
1. Download ssd_mobilenetv2_oidv4 model from [TensorFlow Object Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md)
2. Install TensorFlow [ObjectDetection API](https://github.com/tensorflow/models/tree/master/research/object_detection)
3. Run the following code from research folder (D:\src_code\models\research in my example)
```
set PYTHONPATH=D:\src_code\models\research;D:\src_code\models\research\object_detection;D:\src_code\models\research\slim;%PYTHONPATH%
python object_detection\export_tflite_ssd_graph.py --pipeline_config_path D:\src_code\DNN_models\object_detection\ssd_mobilenet_v2_oid_v4_2018_12_12\pipeline.config  --trained_checkpoint_prefix D:\src_code\DNN_models\object_detection\ssd_mobilenet_v2_oid_v4_2018_12_12\model.ckpt --output_directory D:\src_code\mobile\MADE-mobile-image-processing\lesson7\src\ObjectDetection\app\src\main\assets --max_detections 30
```
4. Run the following code from lesson7\src\ObjectDetection folder
```
python to_tflite.py
```