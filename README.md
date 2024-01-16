# llm_evaluation_llm_with_rust


LLM with Rust 

1. Open the Github codespace & install rust with ```curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh```

2. Configure Rust - ```source "$HOME/.cargo/env"```
   
3. Install Rust LLM framework - Huggingface candle ```git clone https://github.com/huggingface/candle.git```

4. Run the below command to run a simple LLM inference
   
   cargo run --example phi --release -- \
  --prompt "Explain how to find the median of an array and write the corresponding python function.\nAnswer:" \
  --quantized --sample-len 200

5. 
