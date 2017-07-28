#Recommended Directory Structure for Training and Evaluation

+data
  -label_map file
  -train TFRecord file
  -eval TFRecord file
+models
  +model
    -pipeline config file
    +train
    +eval

#Set pipeline config file


#Training

python object_detection/train.py     --logtostderr     --pipeline_config_path=/home/user/MyWorks/owndata/models/model/pipeline_conifig.pbtxt          --train_dir=${HOME}/MyWorks/owndata/models/model/train

#Evaluating

python object_detection/eval.py \
    --logtostderr \
    --pipeline_config_path=/home/user/MyWorks/owndata/models/model/pipeline_conifig.pbtxt \
    --checkpoint_dir=${HOME}/MyWorks/owndata/models/model/train \
    --eval_dir=${HOME}/MyWorks/owndata/models/model/eval

##Note:(Training and testing executed from from 'tensorflow/models' directory)
