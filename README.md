# kaggle_hms
https://www.kaggle.com/competitions/hms-harmful-brain-activity-classification
# training
```
export PYTHONWARNINGS="ignore"
export CUBLAS_WORKSPACE_CONFIG=:4096:8
torchrun --nnodes=1 --nproc_per_node=2 --rdzv_id=100 --rdzv_backend=c10d --rdzv_endpoint=localhost:29400 code/run_train.py --exp exp_stage1_6; torchrun --nnodes=1 --nproc_per_node=2 --rdzv_id=100 --rdzv_backend=c10d --rdzv_endpoint=localhost:29400 code/run_train.py --exp exp_stage2_6
```