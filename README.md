# Time-LLM

金沢大学ICNLサーバ向けに最適化された Time-LLM

---

## 📝 概要

本リポジトリは以下の環境向けに事前設定されています。

- **環境**：金沢大学 ICNL サーバ  
- **GPU**：**2枚の NVIDIA RTX 5000** を使用  
- **混合精度**：**bfloat16 (BF16) を強制**

---

## ⚠️ 注意事項

1. **PyTorch 2.2.2 のインストール**  
   ```bash
   conda install pytorch==2.2.2 torchvision==0.17.2 torchaudio==2.2.2 pytorch-cuda=12.1 -c pytorch -c nvidia
   ```
2. **Accelerate の初期設定**  
   以下の質問には矢印キーで選択し、Enter キーで確定してください。  
   特に最後の混合精度では **`bf16`** を選択してください。

   ```
   In which compute environment are you running?
   ➔ This machine
     AWS (Amazon SageMaker)

   Which type of machine are you using?
     No distributed training
     multi-CPU
   ➔ multi-GPU
     TPU
     MPS

   How many different machines will you use (use more than 1 for multi-node training)? [1]: 1

   Do you wish to optimize your script with torch dynamo? [yes/NO]: NO
   Do you want to use DeepSpeed? [yes/NO]: NO
   Do you want to use FullyShardedDataParallel? [yes/NO]: NO
   Do you want to use Megatron-LM? [yes/NO]: NO

   How many GPU(s) should be used for distributed training? [1]: 2
   What GPU(s) (by id) should be used for training on this machine as a comma-separated list? [all]: 0,1

   Do you wish to use FP16 or BF16 (mixed precision)?
     no
     fp16
   ➔ bf16

   Accelerate configuration saved at ~/.cache/huggingface/accelerate/default_config.yaml
   ```

---

## 📥 参考

- GitHub リポジトリ:  
  https://github.com/KimMeen/Time-LLM.git

