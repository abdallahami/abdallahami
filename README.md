# abdallahami
import numpy as np


class Neroun:
    def __init__(self):
        np.random.seed(1)
        self.random_weights = 2 * np.random.random((3, 1)) - 1
        # input dataset

        self.training_inputs = np.array([[0, 0, 1],
                                         [1, 1, 1],
                                         [1, 0, 1],
                                         [0, 1, 1]])
        # output dataset
        training_outputs = np.array([[0, 1, 1, 0]]).T

     def sigmoid(self,value):
        return 1 / (1 + np.exp(-value))

    def activationFunction(self):
        self.output = np.dot(self.training_inputs, self.random_weights)
        self.activiation_output = self.sigmoid(self.output)
        return self.activiation_output


fneroun = Neroun()
print(fneroun.activationFunction())
