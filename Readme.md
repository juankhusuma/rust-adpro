![Commit 2 screen capture](commit2.png)

![Commit 3 screen capture](commit3.png)

# Commit 4 Reflection Notes
Whenever a request is sent to ```http://127.0.0.1:7878/sleep``` the thread will sleep for 10 seconds, due to the http server being single-threaded, the server can't serve any other request for the entire 10 seconds. The server is forced to handle one request at a time, this will cause a huge latency problem.

#  Commit 5 Reflection Notes
The server is now multi-threaded, using ThreadPool as a way to handle multiple requests at the same time. The thread pool helps prevent the server from being overwhelmed by the number of requests by limiting the number of threads that can be created. The server can now handle multiple requests at the same time, now the server doesn't halt anytime the sleep endpoint is requested and the latency problem is solved.