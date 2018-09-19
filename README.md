# Learning2Ask_TypedDecoder
---
This is the bug fixed version of the code for the paper [Learning to Ask Questions in Open-domain Conversational Systems with Typed Decoders](https://arxiv.org/pdf/1805.04843.pdf) on ACL2018

### Bug Fixes and Other Changes
* Removed the module ```wordseg_python``` that causes bugs.
* Changed style of some codes to make them more readable.


Cite this paper:
```
@inproceedings{wang2018learning,
  title={Learning to Ask Questions in Open-domain Conversational Systems with Typed Decoders},
  author={Wang, Yansen and Liu, Chenyi and Huang, Minlie and Nie, Liqiang},
  booktitle={ACL},
  year={2018}
}
```

## Usage:
**IMPORTANT NOTE: Our code is not compatible with new versions of tensorflow, so please use tensorflow-1.0.0 to run our codes.**

### STD:
Command ```python main.py {--[option1]=[value1] --[option2]=[value2] ... }```

Options(=[default_value]):
* ```--is_train=True``` Set to True for training and False from inference.
* ```--symbols=20000``` Size of vocabulary.
* ```--embed_units=100``` Size of word embedding.
* ```--units=512``` Size of each model layer.
* ```--layers=4``` Number of layers in the model.
* ```--batch_size=50``` Batch size to use during training. 
* ```--data_dir=./data``` Data directory.
* ```--train_dir=./train``` Training directory.
* ```--per_checkpoint=1000``` How many steps to do per checkpoint.
* ```--check_version=0``` The version for continuing training or for inferencing. Set to 0 if you don't want to continue from an existed checkpoint.
* ```--log_parameters=True``` Set to True to show the parameters.
* ```--inference_path=""``` Set filename of inference, empty for screen input.
* ```--PMI_path=./PMI``` PMI directory.
* ```--keywords_per_sentence=20``` How many keywords will be included. We don't need to set this flag in STD.
* ```--question_data=True``` **(Deprecated, please set to True)** An unused option in the final version.

The file ```train.sh``` and ```infer.sh``` contain example commands for training and inference. You can use them with the ```sh``` command.

### HTD:
Command ```python main.py {--[option1]=[value1] --[option2]=[value2] ... }```

Options(=[default_value]):
* ```--is_train=True``` Set to True for training and False from inference.
* ```--symbols=20000``` Size of vocabulary.
* ```--embed_units=100``` Size of word embedding.
* ```--units=512``` Size of each model layer.
* ```--layers=4``` Number of layers in the model.
* ```--batch_size=50``` Batch size to use during training. **Please set to 1 during inference or the PMI mechanism can't work properly.**
* ```--data_dir=./data``` Data directory.
* ```--train_dir=./train``` Training directory.
* ```--per_checkpoint=1000``` How many steps to do per checkpoint.
* ```--check_version=0``` The version for continuing training or for inferencing.
* ```--log_parameters=True``` Set to True to show the parameters.
* ```--inference_path=""``` Set filename of inference, empty for screen input.
* ```--PMI_path=./PMI``` PMI directory.
* ```--keywords_per_sentence=20``` How many keywords will be included.
* ```--question_data=True``` **(Deprecated, please set to True)** An unused option in the final version.

The file ```train.sh``` and ```infer.sh``` contain example commands for training and inference. You can use them with the ```sh``` command.
