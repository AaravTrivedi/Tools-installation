# Overview:

The journey of building a processor starts with a simple C model. This acts as a high-level blueprint of how the RISC-V processor should work. We run applications on it using tools like RISC-V GCC to make sure the design behaves correctly. Once we’re confident, this C model becomes our reference.

Next, we write the actual processor in Verilog. Here, we only describe the core logic and instruction set, while peripherals are added separately as reusable IP blocks. By combining the processor core with these blocks, we get a complete System on Chip (SoC). To verify it, we run the same programs on both the C model and the Verilog model and compare the results.

Unlike microprocessors, which only contain the CPU and rely on external memory and peripherals, microcontrollers pack everything—CPU, memory, and peripherals—into one chip. This makes microcontrollers cheaper, more power-efficient, and better for specific embedded tasks.

Once the Verilog design is ready, it is converted into gates and transistors, then placed and routed into a physical chip layout. This produces a GDS2 file, which is checked for errors before being sent for fabrication (tape-out). Months later, the factory sends back the finished chips (tape-in). We connect peripherals, load programs, and test them to make sure all outputs match our reference model.

The full cycle—from C model to tested silicon—can take more than a year, with final processors usually running at around 100–130 MHz. Fun fact: even the original Arduino used a RISC-V–based chip!

# Yosys

<img width="836" height="684" alt="Screenshot from 2025-09-20 17-46-02" src="https://github.com/user-attachments/assets/478753d8-0e9a-4b09-8cae-b8a5b044a587" />

# iverilog

<img width="779" height="251" alt="image" src="https://github.com/user-attachments/assets/5f9f890f-664f-448d-b69f-c975b86f72e5" />

# GTKwave
<img width="686" height="130" alt="Screenshot from 2025-09-20 17-49-04" src="https://github.com/user-attachments/assets/8f284e5c-3ce1-4d10-9d2f-6b7c1d00ba94" />
<img width="1027" height="685" alt="Screenshot from 2025-09-20 17-49-15" src="https://github.com/user-attachments/assets/50101ec6-07fc-4b10-8b94-014100235775" />

# ngspice
<img width="1152" height="320" alt="Screenshot 2025-09-20 205701" src="https://github.com/user-attachments/assets/360d1f92-1796-493a-90f7-7cceb3345020" />

# magic
<img width="2189" height="1185" alt="Screenshot 2025-09-20 211206" src="https://github.com/user-attachments/assets/6910c42e-b604-4dda-9e1a-c050afb21668" />

# Docker
<img width="1146" height="651" alt="Screenshot 2025-09-20 213438" src="https://github.com/user-attachments/assets/8623490a-98e3-4d17-8c9d-aa0b8ca6d9c8" />

# Dependencies
<img width="1435" height="1384" alt="Screenshot 2025-09-20 213630" src="https://github.com/user-attachments/assets/25aad49f-2c77-435f-9408-a0eb0945dce5" />

