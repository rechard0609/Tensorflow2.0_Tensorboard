# Tensorflow2.0_Tensorboard

#.macos
   - Mojave
   - 10.14.6
   
#.version
scipy 1.4.1
numpy 1.18.5
matplotlib 3.3.0
pandas 1.1.0
sklearn 0.23.1
pydot 1.4.1
h5py 2.10.0
theano 1.0.5
tensorflow 2.3.0
keras 2.4.3
Python 3.8.3

#.tensorboard

setting
...
logdir = "/Users/richardchung/PycharmProjects/keras_talk/logs/scalars/" + datetime.now().strftime("%Y%m%d-%H%M%S")
tensorboard_callback = keras.callbacks.TensorBoard(log_dir=logdir)
...
training_history = model.fit(
    x_train, # input
    y_train, # output
    batch_size=train_size,
    verbose=0, # Suppress chatty output; use Tensorboard instead
    epochs=100,
    validation_data=(x_test, y_test),
    callbacks=[tensorboard_callback],
)
