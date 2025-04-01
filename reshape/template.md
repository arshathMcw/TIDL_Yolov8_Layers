## Reshape
```py
input_layer = tf.keras.Input(shape=(80, 80, 144), batch_size=1, dtype=tf.float32, name="model_22_Concat_output")
reshape_layer = tf.keras.layers.Reshape((144,6400, 1), name="model_22_Reshape")(input_layer)
model = tf.keras.Model(inputs=input_layer, outputs=reshape_layer)
converter = tf.lite.TFLiteConverter.from_keras_model(model)
converter.experimental_new_converter = True 
converter.allow_custom_ops = True
tflite_model = converter.convert()
open(models_path + "210_reshape_layer_ip1x144x80x80_op1x144x6400.tflite", "wb").write(tflite_model)
```