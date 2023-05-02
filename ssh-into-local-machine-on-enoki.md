# SSH Into Local Machine on Enoki

With Enoki, you can easily SSH into your local machine to run your code using local compute. With this, you will benefit from Enoki's multiplayer functionality, while keeping your dev environment the same.

1\) To start, sign up with a free account on ngrok [https://ngrok.com/](https://ngrok.com/). This is a secure SSH tunneling solution&#x20;

2\) Start your ssh server on your respective OS: \
\
For **Mac**, follow this: [https://support.apple.com/lt-lt/guide/mac-help/mchlp1066/mac](https://support.apple.com/lt-lt/guide/mac-help/mchlp1066/mac)\
\
For **Windows**, follow this: [https://woshub.com/connect-to-windows-via-ssh/](https://woshub.com/connect-to-windows-via-ssh/)\
\
For **Linux**, follow this: [https://www.cyberciti.biz/faq/ubuntu-linux-install-openssh-server/](https://www.cyberciti.biz/faq/ubuntu-linux-install-openssh-server/)

3\) Retrieve your free authtoken from ngrok ([https://dashboard.ngrok.com/get-started/your-authtoken](https://dashboard.ngrok.com/get-started/your-authtoken)) and run the following with your local terminal:\
`ngrok config add-authtoken <authtoken>`\
`ngrok tcp 22`

You'll see ngrok forwarding traffic to something like this: `tcp://<ngrok_number>.tcp.ngrok.io:<port>`

4\) On an Enoki workspace, open terminal and ssh into your local machine using this: `ssh -p <port> user@<ngrok_number>.tcp.ngrok.io` \
