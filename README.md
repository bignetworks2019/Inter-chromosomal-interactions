# Inter-chromosomal-interactions

This repository provides a tool to analyze and output significant inter-chromosomal interactions of a given dataset.

### Basic Usage

#### Example
To run the tool on the oocyte_NSN data, execute the following command from the project home directory:<br/>
	``python src/main.py --data "sample-data/data" --bin-size "500k" --config-file "metadata/mm9_chrom_sizes.txt" --output "sample-data/output_oocyte_NSN_500k.txt"``
  
Above command provides the bin size as 500,000. 
  
#### Options
You can check out the other options available to use with the tool using:<br/>
	``python src/main.py --help``
  
#### Input
The supported input format is a list of files consists of links. Each file should have the format:

    chromosome_1 coordinate_1 chromosome_2 coordinate_2 weight
    
#### Output
The output file lists *n* significant inter chromosomal interactions identified. 
The *n* lines are as follows:

	bin_1 bin_2 count p_value

where bins are represented as the size given in the input command.
