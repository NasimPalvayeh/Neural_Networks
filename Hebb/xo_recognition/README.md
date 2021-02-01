In this assignment, we want to use hebb network to implement a method to classify the pattern to be able to distinguish X and O characters.

Initially, two folders, train and test, were created to store images for training and testing.

After running the program, the program will ask you to specify whether you want to teach the program or test.

The train function works as follows:

1. Reads the images in the train folder and converts them to an array of pixels
(Images are 200 * 200, so each image has a row and 40,000 columns, which is 1 (For pixels in black) and -1 (for pixels in white) is filled).
2. It then saves all the images named X as an array in a list called arr_img_x.
3. It also stores all O-named images as arrays in a list called arr_img_o.
4. It then merges the two lists arr_img_x and arr_img_o and puts them in a list called arr_img.
5. Then, according to the following relation, it updates the weights and bias:
w (new) = w (old) + x y
b (new) = b (old) + 1×y
6. Then, returns w and b as the output of the function.

The test function works as follows:

1. It has two inputs w and b
2. First, it reads your drawn image and converts it back to an array of pixels
(the image is 200 x 200, so it has a row and 40,000 columns, which is 1 (for black pixels) and -1 (For white pixels) and stored in img).
3. Then multiply the img and w and add them together and then adds it with b. Sets the result in the yIN variable.
4. Returns one of two values, 1 and -1.

In the main body of the program, first the train function is executed and its outputs are given as input to the test function.

The output value of the test function, if it is equal to 1, your drawn image will be X, and if it is equal to - 1, your drawn image will be O.
Otherwise, an error has occurred.


