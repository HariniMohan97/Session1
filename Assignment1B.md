
1)What are Channels and Kernels (according to EVA)?

Kernals
Kernels are the feature extractors in the form of filters. These kernels are numpy matrices that convolve over another matrix (mostly holding the pixel intensity values) of an image from which we want to extract the features. Each filter is said to extract one set or type of features and hence one filter can have several kernals giving out several output matrices(output of convolution of each kernal with image matrix) that can later be added with one another to give one output for one filter containing many kernals. 

Channels
The input image can consist of several channels or be divided into several channels. Like RGB images can have 3 channels each being a matrix of respective red, blue and green values. So a channel is simply the input matrix of the image from which the feature is being extracted from. Like input channels, there are output channels which are nothing but the output of the convolution. The number of output channels is equal to the number of filters. 
The number of input channels can be more than 3. Like for example, medical images which have more than 3 channels.

2)Why should we only (well mostly) use 3x3 Kernels?

The following reasons are why we mostly use 3x3 -
-> We can achieve any type of convolution by combining multiple 3x3 convolutions. For example, 2 3x3 convolutions is same as one 5x5 convolutions. 
-> While following the above method, we can also see that the number of arithmetic operations or number of parameters being stored is also brought down drastically from 25 to 18. 

3)How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
"99" 3x3 convolutions are required.
Calculations-
199 ---> 197 ---> 195 ---> 193 ---> 191
---> 189 ---> 187 ---> 185 ---> 183 ---> 181
---> 179 ---> 177 ---> 175 ---> 173 ---> 171
---> 169 ---> 167 ---> 165 ---> 163 ---> 161
---> 159 ---> 157 ---> 155 ---> 153 ---> 151
---> 149 ---> 147 ---> 145 ---> 143 ---> 141
---> 139 ---> 137 ---> 135 ---> 133 ---> 131
---> 129 ---> 127 ---> 125 ---> 123 ---> 121
---> 119 ---> 117 ---> 115 ---> 113 ---> 111
---> 109 ---> 107 ---> 105 ---> 103 ---> 101
---> 99 ---> 97 ---> 95 ---> 93 ---> 91
---> 89 ---> 87 ---> 85 ---> 83 ---> 81
---> 79 ---> 77 ---> 75 ---> 73 ---> 71
---> 69 ---> 67 ---> 65 ---> 63 ---> 61
---> 59 ---> 57 ---> 55 ---> 53 ---> 51
---> 49 ---> 47 ---> 45 ---> 43 ---> 41
---> 39 ---> 37 ---> 35 ---> 33 ---> 31
---> 29 ---> 27 ---> 25 ---> 23 ---> 21
---> 19 ---> 17 ---> 15 ---> 13 ---> 11
---> 9 ---> 7 ---> 5 ---> 3 ---> 1
