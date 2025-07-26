<h1>What is the Event Loop?</h1>
The event loop is the core mechanism in Node.js that handles asynchronous operations. It allows Node.js to perform non-blocking I/O operations despite being single-threaded.

<h1>How It Works (Phases):</h1>
Timers Phase
Executes callbacks from setTimeout() and setInterval().

Pending Callbacks Phase
Executes I/O callbacks deferred to the next loop iteration.

Idle, Prepare Phase
Internal use only.

Poll Phase
Waits for I/O events (like reading from disk/network), and executes their callbacks.

Check Phase
Executes setImmediate() callbacks.

Close Callbacks Phase
Executes close event callbacks, like from socket.destroy().


<h1>Deep Dive Resources:</h1>

[Official Node.js Event Loop Guide](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick)

[Event Loop in Node.js](https://blog.insiderattack.net/nodejs-event-loop-and-libuv-the-nuts-and-bolts-70eb8d8c5f92)

