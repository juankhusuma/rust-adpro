![Commit 2 screen capture](commit2.png)

![Commit 3 screen capture](commit3.png)

# Commit 4 Reflection Notes
Whenever a request is sent to ```http://127.0.0.1:7878/sleep``` the thread will sleep for 10 seconds, due to the http server being single-threaded, the server can't serve any other request for the entire 10 seconds. The server is forced to handle one request at a time, this will cause a huge latency problem.