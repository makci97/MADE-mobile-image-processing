Run the following code from the parent directory before actual build in Android Studio
```
python to_tflite.py "tensorflow_photos\app\src\main\assets\places_event_enet0_augm_ft_sgd_model.pb"
python to_tflite.py "tensorflow_photos\app\src\main\assets\places_event_mobilenet2_alpha=1.0_augm_ft_sgd_model.pb"

python to_pytorch.py 
```