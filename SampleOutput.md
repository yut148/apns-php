## sample\_push.php ##

```
Sat, 25 Dec 2010 21:07:50 +0100 ApnsPHP[3876]: INFO: Trying ssl://gateway.sandbox.push.apple.com:2195...
Sat, 25 Dec 2010 21:07:51 +0100 ApnsPHP[3876]: INFO: Connected to ssl://gateway.sandbox.push.apple.com:2195.
Sat, 25 Dec 2010 21:07:51 +0100 ApnsPHP[3876]: INFO: Sending messages queue, run #1: 1 message(s) left in queue.
Sat, 25 Dec 2010 21:07:51 +0100 ApnsPHP[3876]: STATUS: Sending message ID 1 [custom identifier: Message-Badge-3] (1/3): 167 bytes.
Sat, 25 Dec 2010 21:07:52 +0100 ApnsPHP[3876]: INFO: Disconnected.
```

## sample\_push\_many.php ##

```
Sat, 25 Dec 2010 21:08:49 +0100 ApnsPHP[3881]: INFO: Trying ssl://gateway.sandbox.push.apple.com:2195...
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: INFO: Connected to ssl://gateway.sandbox.push.apple.com:2195.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: INFO: Sending messages queue, run #1: 10 message(s) left in queue.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 1 [custom identifier: Message-Badge-001] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 2 [custom identifier: Message-Badge-002] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 3 [custom identifier: Message-Badge-003] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 4 [custom identifier: Message-Badge-004] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 5 [custom identifier: Message-Badge-005] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 6 [custom identifier: Message-Badge-006] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 7 [custom identifier: Message-Badge-007] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 8 [custom identifier: Message-Badge-008] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 9 [custom identifier: Message-Badge-009] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:50 +0100 ApnsPHP[3881]: STATUS: Sending message ID 10 [custom identifier: Message-Badge-010] (1/3): 65 bytes.
Sat, 25 Dec 2010 21:08:51 +0100 ApnsPHP[3881]: ERROR: Unable to send message ID 5: Invalid token (8).
Sat, 25 Dec 2010 21:08:51 +0100 ApnsPHP[3881]: INFO: Disconnected.
Sat, 25 Dec 2010 21:08:51 +0100 ApnsPHP[3881]: INFO: Trying ssl://gateway.sandbox.push.apple.com:2195...
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: INFO: Connected to ssl://gateway.sandbox.push.apple.com:2195.
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: INFO: Sending messages queue, run #2: 6 message(s) left in queue.
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: WARNING: Message ID 5 [custom identifier: Message-Badge-005] has an unrecoverable error (8), removing from queue without retrying...
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: STATUS: Sending message ID 6 [custom identifier: Message-Badge-006] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: STATUS: Sending message ID 7 [custom identifier: Message-Badge-007] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: STATUS: Sending message ID 8 [custom identifier: Message-Badge-008] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: STATUS: Sending message ID 9 [custom identifier: Message-Badge-009] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:08:52 +0100 ApnsPHP[3881]: STATUS: Sending message ID 10 [custom identifier: Message-Badge-010] (1/3): 65 bytes.
Sat, 25 Dec 2010 21:08:53 +0100 ApnsPHP[3881]: INFO: Disconnected.
```

## sample\_feedback.php ##

```
Mon, 01 Mar 2010 22:17:41 +0100 ApnsPHP[421]: INFO: Trying ssl://feedback.sandbox.push.apple.com:2196...
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: Connected to ssl://feedback.sandbox.push.apple.com:2196.
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: Reading...
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: Reading...
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: 114 bytes read.
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: New feedback tuple: timestamp=1267478249 (2010-03-01 22:17:29), tokenLength=32,
                                                    deviceToken=e3434b98811836079119bbb8617373073292d045dc195e87de5765ebae5e50d7.
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: New feedback tuple: timestamp=1267478253 (2010-03-01 22:17:33), tokenLength=32,
                                                    deviceToken=e3434b98811836079119bbb8617373073292d045dc195e87de5765ebae5e50d7.
Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: New feedback tuple: timestamp=1267478256 (2010-03-01 22:17:36), tokenLength=32,
                                                    deviceToken=e3434b98811836079119bbb8617373073292d045dc195e87de5765ebae5e50d7.

[var_dump]

Mon, 01 Mar 2010 22:17:44 +0100 ApnsPHP[421]: INFO: Disconnected.
```

## sample\_server.php ##

```
Sat, 25 Dec 2010 21:05:50 +0100 ApnsPHP[3870]: INFO: Forked process PID 3872
Sat, 25 Dec 2010 21:05:50 +0100 ApnsPHP[3870]: INFO: Forked process PID 3873
Sat, 25 Dec 2010 21:05:50 +0100 ApnsPHP[3872]: INFO: Trying ssl://gateway.sandbox.push.apple.com:2195...
Sat, 25 Dec 2010 21:05:50 +0100 ApnsPHP[3873]: INFO: Trying ssl://gateway.sandbox.push.apple.com:2195...
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: INFO: Connected to ssl://gateway.sandbox.push.apple.com:2195.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: INFO: Process 1 has 5 messages, sending...
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: INFO: Sending messages queue, run #1: 5 message(s) left in queue.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: STATUS: Sending message ID 1 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: STATUS: Sending message ID 2 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: STATUS: Sending message ID 3 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: STATUS: Sending message ID 4 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3872]: STATUS: Sending message ID 5 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: INFO: Connected to ssl://gateway.sandbox.push.apple.com:2195.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: INFO: Process 2 has 4 messages, sending...
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: INFO: Sending messages queue, run #1: 4 message(s) left in queue.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: STATUS: Sending message ID 1 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: STATUS: Sending message ID 2 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: STATUS: Sending message ID 3 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:51 +0100 ApnsPHP[3873]: STATUS: Sending message ID 4 [custom identifier: unset] (1/3): 64 bytes.
Sat, 25 Dec 2010 21:05:52 +0100 ApnsPHP[3873]: INFO: Process 2 has 1 messages, sending...
Sat, 25 Dec 2010 21:05:52 +0100 ApnsPHP[3873]: INFO: Sending messages queue, run #1: 1 message(s) left in queue.
Sat, 25 Dec 2010 21:05:52 +0100 ApnsPHP[3873]: STATUS: Sending message ID 1 [custom identifier: unset] (1/3): 65 bytes.

^C

Sat, 25 Dec 2010 21:07:10 +0100 ApnsPHP[3872]: INFO: Child 3872 received signal #2, shutdown...
Sat, 25 Dec 2010 21:07:10 +0100 ApnsPHP[3873]: INFO: Child 3873 received signal #2, shutdown...
Sat, 25 Dec 2010 21:07:10 +0100 ApnsPHP[3870]: INFO: Parent shutdown, cleaning memory...
```


## <font color='red'>Please, use <a href='https://groups.google.com/group/apns-php'>ApnsPHP Google Group</a> for help requests or to discuss about this project. To report an issue use <a href='http://code.google.com/p/apns-php/issues/list'>Issues</a>. Thanks!</font> ##