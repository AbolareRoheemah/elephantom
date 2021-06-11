<template>
  <div>
    <div class="container">
        <table class="table-container">
            <thead>
              <tr><h5>All Elephants</h5></tr>
              <tr class="table-head">
                <th
                v-for="(th,index) in tableHead"
                :key="index"
                >{{th }}</th>
            </tr>
            </thead>
            <tbody v-for="(el, index) in elephants"
            :key="index">
              <NuxtLink :to="{ name: 'elephants-elephant', params: { elephant: el._id }}"><tr>
                <td class="user-id">
                    {{ index }}
                    </td>
                <td>{{ el.name }}</td>
                <td>{{ el.species }}</td>
                <td>{{ el.sex }} </td>
                <td>{{ el.affiliation }}</td>
                <td>{{ el.dob }}</td>
            </tr></NuxtLink>
            </tbody>
        </table>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
      tableHead: ['S/N', 'Name', 'Species', 'Sex', 'Affliation', 'Dob'],
      elephants: '',
      }
    },
    methods: {
      getElephants() {
      let baseUrl = 'https://elephantapimary3.herokuapp.com'
      fetch(baseUrl + '/elephants')
      .then(res => res.json())
      .then((data) => {
        this.elephants = data.elephants
      })
        return this.elephants 
      },
    },
    created () {
      this.getElephants()
    },
  }
</script>

<style lang="css" scoped>
.container {
  background: #FFFFFF;
box-shadow: 0px 3px 10px -3px rgba(0, 0, 0, 0.25);
padding-bottom: 10vh;
}

table {
    width: 100%;
    height: auto;
    /* border-radius: 5px; */
    margin-top: 5px;
}

tr{
    display: flex;
    justify-content: space-between;
    height: 50px;
    align-items: center;
    padding: 10px;
}
a {
  text-decoration: none;
}
/* td:last-child{
    border-radius: 0 0 5px 5px;
} */

.table-head{
    background: #e5e5e5 !important;
}

th{
    font-family: Overpass;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 28px;
    color: #000000;
}

th,td{
    width: 20%;
    display: flex;
    justify-content: flex-start;
    padding: 20px;
}

tr:nth-child(even) {
    background: #f5f5f5;
}
  
tr:nth-child(odd) {
    background-color: #fff;
}
h5 {
  font-family: Overpass;
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: 28px;
  color: #30425A;
  padding-left: 1vw;
}
td {
  font-family: Overpass;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 25px;
  color: #848383;
}
thead tr:nth-child(1) {
  height: 60px;
}
</style>