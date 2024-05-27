# Github-Action-Yml-to-deploloy-HTML-website-Via-SSH-to-server
This yml file can push website to server via ssh. 




## Deployment

You can copy code from here also!!

```yml
  name: Deploy Website

on:
  push:
    branches:
      - main  # Adjust this to match your main branch

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Install SSH key
        uses: webfactory/ssh-agent@v0.5.3
        with:
          ssh-private-key: ${{ secrets.SECRET_GURA }}

      - name: Deploy website via SSH
        run: |
          scp -o StrictHostKeyChecking=no -r ./* server_user_name_here@server_ip_here:/path/to/destination
```




## Installation

Simply add your workflow with html and change the code with your references.

    
## Modified love with KDJ & ShayC & ZEUS

- [@zeusielk](https://www.github.com/zeusielk)
- [@noobconner21](https://www.github.com/noobconner21)

