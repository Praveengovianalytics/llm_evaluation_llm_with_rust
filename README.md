# llm_evaluation_llm_with_rust


LLM with Rust 

1. Open the Github codespace & install rust with ```curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh```

2. Configure Rust - ```source "$HOME/.cargo/env"```
   
3. Install Rust LLM framework - Huggingface candle ```git clone https://github.com/huggingface/candle.git```

4. Run the below command to run a simple LLM inference
   
   cargo run --example phi --release -- --prompt "Explain how to find the median of an array and write the corresponding python function.\nAnswer:" --quantized --sample-len 200

5. Build the simple app , Compile & Run

cargo new my_first_app 
cargo build 
cargo run

6. Build simple app & run neural network

cargo new my_second_app
cd my_second_app 
cargo add --git https://github.com/huggingface/candle.git candle-core

use candle_core::{Device, Tensor};

fn main() -> Result<(), Box> { let device = Device::Cpu;

let a = Tensor::randn(0f32, 1., (2, 3), &device)?;
let b = Tensor::randn(0f32, 1., (3, 4), &device)?;

let c = a.matmul(&b)?;
println!("{c}");
Ok(())
}
