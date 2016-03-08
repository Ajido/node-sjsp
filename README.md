# node-sjsp  - Simple JavaScript Profiler

```bash
# Warning: this operation is destructive.
$ cd YOUR_NODEJS_PROJECT_ROOT
$ npm install https://github.com/Ajido/node-sjsp.git
$ find src -name '*.js' | while read FILE; do
    node_modules/.bin/sjsp $FILE
    cp $FILE ${FILE}.orig
    mv `echo $FILE | sed 's/\.js$/\.sjsp.js/'` $FILE
  done
$ node MAIN_SCRIPT.JS
```

```
========== SORT BY TIME ==========
total:  0.01sec   count:  157    src/b.js   b  (line:   1, col: 14)   function b() {
total:  0.00sec   count:  103    src/a.js   a  (line:   3, col: 14)   function a() {
========== SORT BY COUNT ==========
total:  0.01sec   count:  157    src/b.js   b  (line:   1, col: 14)   function b() {
total:  0.00sec   count:  103    src/a.js   a  (line:   3, col: 14)   function a() {
```

## Original

- https://github.com/itchyny/sjsp
- https://github.com/45deg/node-sjsp
