# TensorFlow Lab Offered by Google
Codelabs Tensorflow teaching on Machine Vision and feature scoring.
This is my attempt at working my way through the various modules and setup sections.

# Basic Introduction
The codelabs portion for this tutorial is found here:
https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/#0

This project is being conducted on an Arch Linux virtual machine. The following instructions involve the basic setup for the project.
```bash
$ sudo pacman -S tensorflow tensorboard
$ sudo pip2 install -r requirements.pip
$ # Run the setup script...
$ . ./setup
```

To train the network, you'll need to run the following:

```bash
$ cd tensorflow-for-poets-2
$ python -m scripts.retrain \
  	 --bottleneck_dir=../tf_files/bottlenecks \
	 --how_many_training_steps=500 \
	 --model_dir=../tf_files/models/ \
	 --summaries_dir=../tf_files/training_summaries/"${ARCHITECTURE}" \
	 --output_graph=../tf_files/retrained_graph.pb \
	 --output_labels=../tf_files/retrained_labels.txt \
	 --architecture="${ARCHITECTURE}" \
	 --image_dir=../tf_files/flower_photos
```

# Docker Composition


