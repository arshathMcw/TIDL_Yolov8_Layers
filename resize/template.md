## Resize 
```py
input_layer = tf.keras.Input(shape=(40, 40, 384), dtype=tf.float32, name="model_9_cv2_act_Mul")
resize_layer = tf.keras.layers.Resizing(height=80, width=80, name="model_10_Resize")(input_layer)
model = tf.keras.Model(inputs=input_layer, outputs=resize_layer)
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()
open(models_path + "resize_layer_1x384x40x40_1x384x80x80.tflite", "wb").write(tflite_model)
```