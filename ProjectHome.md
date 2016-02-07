<img src='http://apns-php.googlecode.com/svn/images/icon.png' align='left' width='220' height='180'>
<h1>ApnsPHP: Apple Push Notification & Feedback Provider</h1>

A <b>full set</b> of <i>open source</i> PHP classes to interact with the <b>Apple Push Notification service</b> for the iPhone, iPad and the iPod Touch.<br>
<br>
<ul><li><a href='https://github.com/duccio/ApnsPHP/blob/master/sample_push.php'>Sample PHP Push code</a>
</li><li><a href='https://github.com/duccio/ApnsPHP/blob/master/sample_feedback.php'>Sample PHP Feedback code</a>
</li><li><a href='https://github.com/duccio/ApnsPHP/blob/master/sample_server.php'>Sample PHP Server code</a>
</li><li><a href='http://code.google.com/p/apns-php/wiki/ObjectiveC'>Sample Objective-C device code</a></li></ul>

<a href='http://code.google.com/p/apns-php/wiki/CertificateCreation'>How to generate a Push Notification certificate and download the Entrust Root Authority certificate</a>
<br><br>

<h2>Source Code</h2>

To be sure to obtain the latest version <a href='https://github.com/duccio/ApnsPHP'>clone the repository on github</a>.<br>
<br>
<h2>News</h2>

<ul><li><b>October 26, 2012</b>, Project source code has <b><a href='https://github.com/duccio/ApnsPHP'>moved to github</a></b>.<br>
</li><li><b>June 18, 2011</b>, Please, use <b><a href='https://groups.google.com/group/apns-php'>ApnsPHP Google Group</a></b> for help requests or to discuss about this project. To report an issue use <b><a href='http://code.google.com/p/apns-php/issues/list'>Issues</a></b>. Thanks!<br>
</li><li><b>December 18, 2010</b>, Full APNs message support: <b>message body</b>, <b>localized action button</b>, <b>localized message</b> with <b>arguments substitution</b> and <b>custom launch images</b>.<br>
</li><li><b>December 15, 2010</b>, Committed the first version of the Objective-C Demo Project with not-running, running in foreground and running in background application state support.<br>
</li><li><b>December 14, 2010</b>, Added the support for <b>multiple Custom Property</b>.<br>
</li><li><b>August 28, 2010</b>, Added support for the <b>new APNs enhanced format</b> that addresses some of the issues with the simple format: <b>Notification expiry</b> and <b>Error response</b>.<br>
</li><li><b>February 28, 2010</b>, ApnsPHP Source Code is now available.</li></ul>

<h2>Please...</h2>
... drop a line if you use ApnsPHP for your published application on the App Store! Thanks :-)<br>
<br>
<h2>Features</h2>

<ul><li><b>Autoload system</b>, explicitly include only Autoload.php and all classes are loaded on-demand.<br>
</li><li><b>Message class</b>, to build a notification payload.<br>
</li><li><b>Push class</b>, to push one or more messages to Apple Push Notification service.<br>
</li><li><b>Feedback class</b>, to query the Apple Feedback service to get the list of broken device tokens.<br>
</li><li><b>Push Server class</b>, to create a Push Server with one or more (forked) processes reading from a common message queue.<br>
</li><li><b>Log class/interface</b>, to log to standard output or for custom logging purpose.<br>
</li><li><b>Objective-C Demo Project</b> with <i>not-running</i>, running in <i>foreground</i> and running in <i>background</i> application state support.</li></ul>

<h2>Classes hierarchy</h2>

<img src='http://apns-php.googlecode.com/svn/images/classes1.png' />

<img src='http://apns-php.googlecode.com/svn/images/classes2.png' />

<img src='http://apns-php.googlecode.com/svn/images/classes3.png' />

<h2>APIs Documentation and Source Code</h2>

<ul><li><a href='http://apns-php.googlecode.com/svn/reference/index.html'>Full APIs Documentation</a>
</li><li><a href='https://github.com/duccio/ApnsPHP'>Full Source Code Library</a>
</li><li><a href='https://github.com/duccio/ApnsPHP/tree/master/Objective-C%20Demo'>Full Source Objective-C Demo Project</a></li></ul>

<h2>Details</h2>

In the Apple Push Notification Binary protocol there isn't a real-time feedback about the correctness of notifications pushed to the server. So, after each write to the server, the Push class waits for the "read stream" to change its status (or at least N microseconds); if it happened and the client socket receives an "end-of-file" from the server, the notification pushed to the server was broken, the Apple server has closed the connection and the client needs to reconnect to send other notifications still on the message queue.<br>
<br>
To speed-up the sending activities the Push Server class can be used to create a Push Notification Server with many processes that reads a common message queue and sends parallel Push Notifications.<br>
<br>
All client-server activities are based on the "on error, retry" pattern with customizable timeouts, retry times and retry intervals.<br>
<br>
<h2>Requirements</h2>

<b><a href='http://www.php.net/'>PHP 5.3.0</a></b>  or later with OpenSSL, PCNTL, System V shared memory and semaphore support.<br>
<br>
<pre><code>./configure --with-openssl[=PATH] --enable-pcntl --enable-sysvshm --enable-sysvsem<br>
</code></pre>

<b>Notice</b>: starting from the <b><a href='https://code.google.com/p/apns-php/source/detail?r=47'>revision 47</a></b> if you plan to use <b>only Push and Feedback</b> provider <b>without the Server</b> part you need <b>only OpenSSL</b> (no PCNTL, System V shared memory or semaphore):<br>
<br>
<pre><code>./configure --with-openssl[=PATH]<br>
</code></pre>

<i>Usually OpenSSL is built-in in standard PHP Linux distributions packages.</i>
<br><i>Standard PHP 5.3.0 shipped with Mac OS X Snow Leopard just works.</i>

<h2>Todo</h2>

<a href='http://code.google.com/p/apns-php/wiki/ToDo'>Todo list on a wiki page</a>