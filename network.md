### Network Format

#### Openpose Backend

##### How to connect

Protocol: tcp

Address: 127.0.0.1

Port: 1234

##### Format of data within a single frame

- Number of persons in the picture (np)
  - unsigned int
  - 4 bytes
  
  **Block A (repeat np times)**
  
  - Number of keypoints of the person (npk)
  
    - unsigned int
    - 4 bytes
  
    **Block A.1 (repeat npk times)**
  
    - X-axis (width)
      - float
      - 4 bytes
    - Y-axis (height)
      - float
      - 4 bytes
    - Prob
      - float
      - 4 bytes
  
- Number of hands in the picture (nh = np * 2)
  - unsigned int
  - 4 bytes
  
  **Block A (repeat nh times)**
  
  - Number of keypoints of the hand (nhk)
  
    - unsigned int
    - 4 bytes
  
    **Block A.1 (repeat nhk times)**
  
    - X-axis (width)
      - float
      - 4 bytes
    - Y-axis (height)
      - float
      - 4 bytes
    - Prob
      - float
      - 4 bytes
  
  



