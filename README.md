# Default starter for Gridsome
`
### 1. Install Gridsome CLI tool if you don't have

`npm install --global @gridsome/cli`

### 2. Create a Gridsome project

1. `gridsome create my-gridsome-site` to install default starter </li>
2. `cd my-gridsome-site` to open folder
3. `gridsome develop` to start local dev server at `http://localhost:8080`
4. Happy coding 🎉🙌
### めも

### sass
```
npm i -D node-sass sass-loader
```
して普通のVueファイルと同じように 
styleにlang指定するだけ
```
<style lang="scss">
```

markdownで書くため
```
npm install @gridsome/source-filesystem @gridsome/transformer-remark
```