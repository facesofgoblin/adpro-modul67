<h1>Commit 1</h1>
<h3>Understanding handle_connection Method</h3>
The handle_connection function is responsible for processing incoming TCP streams. Here's a breakdown of what it does:

1. It takes a mutable reference to a TcpStream as its argument.
2. It creates a BufReader wrapping the given TCP stream. This helps with buffered reading from the stream efficiently.
3. It reads lines from the buffered reader (BufReader) until it reaches an empty line. This is commonly how HTTP requests are formatted, with headers followed by an empty line.
4. It collects these lines into a vector, representing the HTTP request.
5. Finally, it prints out the HTTP request for inspection.
   In summary, handle_connection reads the incoming TCP stream line by line until it encounters an empty line, indicating the end of the HTTP request headers. Then it prints out the collected lines as the HTTP request.

<h1>Commit 2</h1>
<h3>Implement Reading Browser Request</h3>
<br>Implemented a new function, handle_connection, to process connections by reading data from a TCP stream and printing it, allowing inspection of browser-sent data. Updated main.rs with required imports and adjusted the loop to utilize the handle_connection function. The function utilizes BufReader for buffered reading and captures HTTP requests as vectors of strings, printed for verification.</br>
