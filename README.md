# blood_cells_detector-with-Python-OpenCV
_Calculate the average count and speed of blood cells in videos using cv2 and vidstab_

## 1. Preamble
**_Used python modules:_**

_We use numpy module for a wide variety of mathematical operations on arrays and python-opencv module for video processing. Vidstab is used to correct undesirable shakes and jitters when we use hand-held camera and camera mounted on vehicles. tkinter module is responsible for gui part in our project and multiprocessing module can be used for multiprocessing on multi-core computers to boost the performance speed.
Furthermore, we use pyautogui module to select ROI using mouse click and math module for several mathematical operations like sqrt. matplotlib module is used to draw 2D graph for the final results and we import collections module to use python store variable types like tuple, dictionary and list.
Last, we import two customized modules, namely common and video which are responsible for clocking & selection of ROI and processing video including importing, respectively._

https://nanonets.com/blog/optical-flow/

https://adamspannbauer.github.io/python_video_stab/html/index.html

## 2. Result and performance

<p>
<img src="/result/processing_flood_cells.gif">
</p>
<p>
<img src="/result/result.png" width="400" height="300">
</p>

## 3. Implementation
```
from __future__ import print_function

import pyautogui
import math
# from re import S
import numpy as np
import cv2
from vidstab import VidStab
import matplotlib.pyplot as plt
from math import sqrt


from multiprocessing.pool import ThreadPool
from collections import deque
import tkinter as tk
from tkinter import filedialog

from common import clock, StatValue , draw_str, RectSelector
import video

class App:

  def __init__(self, propotion,video_src, roiwid, roihei,type, paused = False):
  
  def init_thread(self):
  
  def init_value(self):
  
  def process_frame(self, gFrame, t0, scale):
  
  def cubic_interp1d(self, x0, x, y):
  
  def makeTitleMask(self, frame, proportion = 0.5) : 
  
  def filterProcess(self, gray):
  
  def CropImgByRect(self, img, rect):
  
  def IsExistPoint(self, point, croped_pos):
  
  def AvarageFilter(self, lst, filter_size,total_size):
  
  def filterSize(self, img,filter_1,filter_2):
  
  def GetAverageCount(self, img, filter_1 = 10, filter_2 = 15) : 
  
  def display_flow(self, flow, stride=40):
  
  def onrect(self, rect):
  
  def drawGraph(self, x, y, x_new, avarage,y_lab, title):
  
  def run(self):
  
root = tk.Tk()
root.withdraw()
video_src = filedialog.askopenfilename()
type = input("Input 1 or 0 for type of video ::   ")
if __name__ == '__main__':
    static_ROI = App(0.5,video_src, 50, 200, type, False).run()
  
```
