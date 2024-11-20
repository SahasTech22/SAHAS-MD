<h2>STEP 1 : COPY UNDER WORKFLOW DEPLOYEMNT CODE</h2><br>
<h2>STEP 2 : GO TO YOUR REPO ACTION TAG </h2><br>
<h2>STEP 3 : CLICK "SETUP NEW WORKFLOW"</h2><br>
<h2>STEP 4 : PASTE YOUR WORKFLOW DEPLOYMENT CODE AND SAVE FILE</h2><br>


<p align="center"> 𝗪𝗢𝗥𝗞𝗙𝗟𝗢𝗪 𝗗𝗘𝗣𝗟𝗢𝗬 𝗖𝗢𝗗𝗘</p>
<h6 align-"center">Attention! We do not take responsibility if your github account is suspended through this Deploy method, I advise you not to use this workflow deploy method in the latest github accounts, github accounts created a year or more ago have not received the risk of suspension so far, this works It will only be done for 6 hours, you need to update the code to reactivate it</h6>

```
name: Node.js CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:

    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]

    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}

    - name: Install dependencies
      run: npm install

    - name: Start application
      run: npm start
yarn start
```
