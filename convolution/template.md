## To create convolution model
```py
input_layer = tf.keras.Input(shape=(640, 640, 3), dtype=tf.float32, name="images")
conv_layer = tf.keras.layers.Conv2D(
    filters=48,             
    kernel_size=(3, 3),     
    strides=(2, 2),         
    padding="same",         
    use_bias=True,
    name="model_0_conv"     
)(input_layer)
model = tf.keras.Model(inputs=input_layer, outputs=conv_layer)
```