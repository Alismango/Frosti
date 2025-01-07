---
title: How to install nvm npm
description: Modify the code box style
pubDate: 07 18 2024
image: /image/image1.jpg
categories:
  - tech
tags:
  - npm
  - nvm
  - tech
---

Install rpm

# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

# Download and install Node.js:
nvm install 20

# Verify the Node.js version:
node -v # Should print "v20.18.1".
nvm current # Should print "v20.18.1".

# Verify npm version:
npm -v # Should print "10.8.2".
