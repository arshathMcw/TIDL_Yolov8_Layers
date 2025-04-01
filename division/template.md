## Division Layer
```py
input_layer = tf.keras.Input(shape=(2, 8400), dtype=tf.float32, name="model_22_Add_2_output")
constant_tensor = tf.constant(2.0, shape=(2, 8400), dtype=tf.float32)  
div_layer = tf.keras.layers.Lambda(lambda x: x / constant_tensor, name="model_22_Div_1")(input_layer)
model = tf.keras.Model(inputs=input_layer, outputs=div_layer)
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()
open(models_path + "div_layer_1x2x8400.tflite", "wb").write(tflite_model)
```