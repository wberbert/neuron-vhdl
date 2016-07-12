# neuron-vhdl
Implementation of a neuron in vhdl

## Sigmoid aproximation
Sigmoid function has been implementated with an aproximation based on a ROM. All the code and the whole aproximation is located into the "src/sigmoid.vhd" file. The aproximation mean error 0,00013.

### Sigmoid function, aproximation and error
![alt tag](https://github.com/dicearr/neuron-vhdl/blob/master/img/error_completa.png)

### Aproximation considering codification error and resource limit error.
![alt tag](https://github.com/dicearr/neuron-vhdl/blob/master/img/aprox.png)
![alt tag](https://github.com/dicearr/neuron-vhdl/blob/master/img/aprox_zoom.png)

The error commited due to resource limit means that ROMs size cannot be as big as we want so only a restricted number of entries can be used, the aproximation considering only this error has been painted in blue. Moreover the codification error is related to the fact that we only have 32bits (Q15.16) to codify numbers, this aproximation considering both kind of errors has been painted in violet.

### Error around the zero
![alt tag](https://github.com/dicearr/neuron-vhdl/blob/master/img/error_cero.png)

## IP package
The IP package includes a neuron with 6 inputs. It uses AXI LITE protocol to communicate, and it has been developed for a Zynq ZedBoard.

