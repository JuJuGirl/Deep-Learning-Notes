Slot Filling Problem: 
  问题简述：比如自动订票系统中输入：买一张7月1日飞往台北的机票 (arrive Taibei on July 1st)；买一张7月1日离开台北的机票 (leave Taibei on July 1st).
  Def: slot位置，e.g. 台北是一个城市，属于一个slot城市， 01/07/2019是一个日期，属于另一个slot日期
  Solve: Feedforward network: 
    Input: a word (Each word is represented as a vector)
    Output: Probability distribution that the input word belonging to the slots.
    引入概念： 1-of-N Encoding
             Beyond 1-of-N encoding (add a dimension for "other" )
  新的问题： output无法区分台北是出发地还是到达地 --> 寄希望于neural network是有记忆的，在看到Taibei之前看到过arrive --> 引入RNN
  
RNN: 
  特点：有记忆. The output of hidden layer(neural) are stored in the memory. Memory can be consisted as another input.
  e.g.
  ![image](屏幕快照 2019-09-20 上午11.13.47)
