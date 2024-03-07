<template>
  <div>
    <div class="container">
      <div class="table-wrapper">
        <table>
          <thead>
            <tr>
              <th>
                <img src="../assets/search.png" alt="#" />
                <b>Business Name</b>
                <img src="../assets/arrow.png" alt="#" />
              </th>
              <th>
                <img src="../assets/cross.png" alt="#" />
                <b>Team</b>
                <img src="../assets/arrow.png" alt="#" />
                <img
                  class="dropdown-arrow"
                  src="../assets/arrow-down.png"
                  alt="#"
                />
              </th>
              <th>
                <img src="../assets/cross.png" alt="#" />
                <b>Role</b>
                <img src="../assets/arrow.png" alt="#" />
                <img
                  class="dropdown-arrow"
                  src="../assets/arrow-down.png"
                  alt="#"
                />
              </th>
              <th>
                <img src="../assets/search.png" alt="#" />
                <b>Gmail</b>
                <img src="../assets/arrow.png" alt="#" />
              </th>
              <th>
                <img src="../assets/cross.png" alt="#" />
                <b>Birthday</b>
                <img src="../assets/arrow.png" alt="#" />
                <img
                  class="dropdown-arrow"
                  src="../assets/arrow-down.png"
                  alt="#"
                />
              </th>
              <th>
                <b>Telegram</b>
                <img src="../assets/arrow.png" alt="#" />
              </th>
              <th>Last Login</th>
              <th>User permissions</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(person, index) in employees" :key="index">
              <td>
                <img :src="person.photo" alt="photo" /><span>{{
                  person.businessName
                }}</span>
              </td>
              <td>{{ person.team }}</td>
              <td>{{ person.role }}</td>
              <td>{{ person.gmail }}</td>
              <td>{{ person.birthday }}</td>
              <td>{{ person.telegram }}</td>
              <td>{{ person.lastLogin }}</td>
              <td>
                <img src="../assets/edit.png" alt="edit" />
                <img class="trash" src="../assets/trash.png" alt="trash" />
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <div class="pagination">
      <img src="../assets/arrow-left.png" alt="arrow-left" />
      <p>1</p>
      <p>2</p>
      <p>3</p>
      <p>...</p>
      <p>12</p>
      <img src="../assets/arrow-right.png" alt="arrow-right" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    employees: Array,
  },
};
</script>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
  padding: 22px 16px;
}

td {
  border-left: none;
  border-right: none;
}

td img {
  margin-right: 10px;
}

td img,
td span {
  vertical-align: middle;
}

tr:last-child td {
  border-bottom: none;
}

tr:first-child td {
  border-top: none;
}

td:last-child {
  border-left: none;
}

th {
  border-top: none;
  border-bottom: none;
  background-color: #f2f2f2;
  padding: 22px 16px;
  background-color: #e5e8ef;
}

th:first-child {
  border-left: none;
  border-radius: 12px 0 0 12px;
}

th:last-child {
  border-right: none;
  border-radius: 0 12px 12px 0;
}

th img,
th b {
  vertical-align: middle;
}

th b {
  padding: 0 4px;
}

th .dropdown-arrow {
  float: right;
}

.trash {
  float: right;
  margin-top: 8px;
}

.container {
  padding: 16px;
  box-sizing: border-box;
  background-color: #fff;
  border-radius: 12px;
  margin-bottom: 28px;
}

.table-wrapper {
  display: block;
  overflow: hidden;
}

.pagination {
  display: flex;
  align-items: center;
  max-width: 100%;
  padding: 16px 28px;
  background-color: #fff;
  border-radius: 10px;
  position: absolute;
  bottom: 28px;
  left: 28px;
  right: 28px;
}

.pagination p {
  padding: 8px 15px;
}

.pagination img:hover,
.pagination p:hover {
  cursor: pointer;
  background-color: #f5f7fb;
}
</style>
