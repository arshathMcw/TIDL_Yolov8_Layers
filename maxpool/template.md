## Maxpool Layer
```py
input_layer = tf.keras.Input(shape=(20, 20, 288), dtype=tf.float32, name="model_9_cv1_act_Mul")
pool_layer_1 = tf.keras.layers.MaxPooling2D(pool_size=(3, 3), strides=(1, 1), padding="same", name="model_9_m_MaxPool_1")(input_layer)
pool_layer_2 = tf.keras.layers.MaxPooling2D(pool_size=(3, 3), strides=(1, 1), padding="same", name="model_9_m_MaxPool_2")(pool_layer_1)
model = tf.keras.Model(inputs=input_layer, outputs=pool_layer_2)
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()
open(models_path + "maxpool_layer_1x288x20x20.tflite", "wb").write(tflite_model)
``