<template>
<div>
    <h1>{{ msg }}</h1>


  <table>
    <thead>
        <tr>
            <th>序号</th>
            <th>书名</th>
            <th>作者</th>
            <th>价格</th>
        </tr>
    </thead>
    <tbody>
        <tr v-for="(item, index) in books" :key="item.name + index">
            <td>{{index+1}}</td>
            <td>{{item.name}}</td>
            <td>{{item.author}}</td>
            <td>{{item.price}}</td>
        </tr>
    </tbody>
  </table>
  <div>
    <p>请输入待添加的图书</p>
    <div>
     <label>书名</label>  <input type="text" v-model="newBookName" /> 
    </div>
    <div>
      <label>作者</label> <input type="text" v-model="newBookAuthor" /> 
    </div>
    <div>
      <label>价格</label> <input type="number" v-model="newBookPrice" /> 
    </div>
  </div>
  <button @click="onAddBook">添加</button>
</div>
</template>

<script>
export default {
  name: 'BookMgr',
  props: {
    msg: String
  },
  data(){
    return{
        books:[
        {name:'西游记',author:'吴承恩',price:98},
        {name:'水浒传',author:'施耐庵',price:96},
        ],
        newBookName:"",
        newBookAuthor:"",
        newBookPrice:0,
        //newBook:{name:"",author:"",price:0},
    }
  },
  methods:{
    onAddBook(){
        let newBook={name:this.newBookName,author:this.newBookAuthor,price:this.newBookPrice}       
        this.books.push(newBook)
        console.log(this.books)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
tbl{
    margin:0 10px;
}
</style>
