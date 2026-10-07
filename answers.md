# OSTEP Ch.4 Homework Answers
## Q1
- Prediction / 预测:7
- Reasoning / 理由:one process with 1 cpu burst and 1 I/O event,cpu takes 2 time units,I/O takes 5,total time is 7
- Verified result / 验证结果:
- Analysis / 分析:
## Q2
- Prediction / 预测:11
- Reasoning / 理由:the first process uses 4 cpu time units.the second process runs for 1 cpu unit and then waits 5 time units for I/O.without overlapping,total time =4+1+5=11
- Verified result / 验证结果:
- Analysis / 分析:
## Q3
- Prediction / 预测：7
- Reasoning / 理由：The first process runs one instruction and then blocks for I/O. While waiting for I/O, the second CPU-bound process can run in parallel with the I/O operation, overlapping CPU work and I/O.
- Verified result / 验证结果：
- Analysis / 分析：
## Q4
- Prediction / 预测：11
- Reasoning / 理由：SWITCH_ON_END means the OS will NOT switch to another process while a process is waiting for I/O. It waits until the whole process finishes before running the next one, so no overlapping occurs.
- Verified result / 验证结果：
- Analysis / 分析：
## Q5
- Prediction / 预测：10
- Reasoning / 理由：Both processes are purely CPU-bound, with no I/O at all. They run sequentially one after another, 5 + 5 = 10 total time. CPU will always be busy.
- Verified result / 验证结果：
- Analysis / 分析：
## Q6
- Prediction / 预测：10
- Reasoning / 理由：Two pure CPU processes still run sequentially even with the SWITCH_ON_IO flag, since neither process triggers any I/O to cause a context switch.
- Verified result / 验证结果：
- Analysis / 分析：
## Q7
- Prediction / 预测：21
- Reasoning / 理由：The first process runs and blocks for I/O. While waiting, the other two CPU processes can run. After I/O completes, the original I/O process resumes immediately because of IO_RUN_IMMEDIATE.
- Verified result / 验证结果：
- Analysis / 分析：
## Q8
- Prediction / 预测：21
- Reasoning / 理由：When I/O completes, IO_RUN_LATER does not immediately run the finished process. The currently running CPU process continues until it finishes.
- Verified result / 验证结果：
- Analysis / 分析：