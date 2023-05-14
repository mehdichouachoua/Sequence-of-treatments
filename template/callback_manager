"""This module contains callback manager for lstm network training"""
from typing import List

class CallbackManager:
    """A class to manage callback functions.

    Attributes:
        _lr_reduce_factor: A float, factor for learning rate reduction.
        _min_delta: A float, minimum value of val loss decreasing.
        _min_lr: A float, minimum allowed value for learning rate.
        _min_loss: A float, default minimum value for learning rate.
    """
    def __init__(self, config):
        """Creates an instance of the class

        Args:
            config: LstmCallbackConfiguration object.
        """
        self._lr_reduce_factor = config["lr_reduce_factor"]
        self._min_delta = config["lr_reduce_min_delta"]
        self._min_lr = config["lr_reduce_min_lr"]
        self._min_loss = 0.0001

    def get_reduced_lr(self, loss: List[float], lr: float) -> float:
        """Returns reduced learning rate.

        Returns:
            A float, reduced learning rate.
        """
        current_min_loss = min(loss)
        if self._min_loss - current_min_loss <= self._min_delta:
            reduced_lr = self._lr_reduce_factor * lr
            if reduced_lr > self._min_lr:
                print('Learning rate reduced from {} to {}'.format(lr, reduced_lr))
                return reduced_lr
            else:
                return lr
        else:
            self._min_loss = current_min_loss
            return lr
