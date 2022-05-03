# Agile-AES
Flexible AES 128, 192, and 256 implementations in Python, C++, Vivado HLS, Chisel and PyRTL, and Verilog

## How to cite

If you use this code, please cite:

X. Guo, M. El-Hadedy, S. Mosanu, X. Wei, K. Skadron, M. Stan, “Agile-AES: Implementation of Configurable AES Primitive with Agile Design Approach”, _Integration, the VLSI Journal,_ 2022. (https://www.sciencedirect.com/science/article/pii/S0167926022000426)

    @article{guo2022agile,
    	  title={Agile-AES: Implementation of configurable AES primitive with agile design approach},
    	  author={Guo, Xinfei and El-Hadedy, Mohamed and Mosanu, Sergiu and Wei, Xiangdong and Skadron, Kevin and Stan, Mircea R},
    	  journal={Integration},
    	  year={2022},
    	  publisher={Elsevier}
    }

## Goals of this work:
- provide a Python and C/C++ implementation - OK
- provide a Vivado HLS implementation - OK
- provide a Chisel implementation - OK
- provide a rocket-chip RoCC accelerator - starting
- provide custom RISC-V instructions - to do
- provide a PyRTL implementation - started
- propose a dual-clock acceleration - to do
- provide a Verilog implementation - OK

## Python implementation details
- `script.py` contains the test run of the cipher and inverse cipher
- `AESfunctions.py` contains the implementation of each of the AES subroutines as well as the Cipher and the Inverse Cipher
- `AEStables.py` contains all the AES tables data
- `devtests.py` can be used as a further scratch-test area
- this is a functional implementation of AES (TODO: OOP version)
- fully parametrizable for all AES versions (128, 192, 256) and other parameters 
- tested in Sublime Text on Windows 10 with Python 3.6 (64-bit)

## C++ implementation details
- supports AES 128, 192 and 256 by allocating memory to accomodate all versions
- tested in Microsoft Visual Studio

## Verilog implementation details
The Verilog implementation provided here is the same exact implementation from Altera's Advanced Synthesis Cookbook, only with the `stratixii_lcell_comb` replaced with a bitwise XOR (`^` in Verilog).

## Useful links:

What's a Creel? YouTube channel has some great videos on explaining and implementing AES
- https://www.youtube.com/user/WhatsACreel/videos
- https://www.youtube.com/playlist?list=PLIBpkBrhT5aBeH_7sSxJAM3XgoCd7nSXS

Link to the AES standard
- https://csrc.nist.gov/csrc/media/publications/fips/197/final/documents/fips-197.pdf

Altera's Advanced Synthesis Cookbook includes an AES 128/256 implementation
- https://www.altera.com/content/dam/altera-www/global/en_US/pdfs/literature/manual/stx_cookbook.pdf
- https://www.altera.com/literature/manual/cookbook.zip

University of Virginia ECE Wiki FPGA tutorials
- http://venividiwiki.ee.virginia.edu/mediawiki/index.php/Xilinx
- http://venividiwiki.ee.virginia.edu/mediawiki/index.php/Altera
- http://venividiwiki.ee.virginia.edu/mediawiki/index.php/ToolsXilinxLabsRTLHLSAES
