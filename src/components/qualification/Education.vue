<template>
  <div class="ed">
    <div class="edu-card">
      <div class="card">
        <div class="school">
          <p class="course">computer science</p>
          <p class="uni">caritas-university</p>
        </div>
        <div class="date">
          <i><img src="../../../public/images/calendar.svg" alt="" /></i>
          <p>2017-2021</p>
        </div>
      </div>
      <div class="card">
        <div class="school">
          <p class="course">web development</p>
          <p class="uni">Microverse</p>
        </div>
        <div class="date">
          <i><img src="../../../public/images/calendar.svg" alt="" /></i>
          <p>2023</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.edu-card {
  display: flex;
  gap: 20px;
}
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 10px;
  gap: 5px;
  margin-top: 1rem;
  /* position: absolute; */
  /* top: 60px; */
  width: 200px;
  height: 150px;
  border: 1px solid #dbdbdb;
  border-radius: 10px;
}
.card:hover {
  background: rgba(255, 255, 255, 0.5);
  border: 1px solid #dbdbdb;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.25);
}
.card .school {
  gap: 29px;
  width: 100%;
  height: 98px;
  /* margin-top: -4em; */
}
.card .school .course {
  width: 100px;
  height: 42px;
  font-weight: 600;
  font-size: 14px;
  line-height: 21px;
  margin-bottom: 3rem;
  color: #383838;
  transform: translateY(1rem);
  transition: 0.25s;
}
.school {
  width: 116px;
  height: 21px;
  font-weight: 600;
  font-size: 14px;
  line-height: 21px;
  color: #383838;
}
.date {
  display: flex;
  width: 100%;
  gap: 10px;
  margin-top: 1em;
}
.date p {
  width: 69px;
  height: 18px;
  font-weight: 400;
  font-size: 12px;
  line-height: 18px;
  color: #616161;
}
.date i {
  transform: translateY(-0.4em);
  height: 0;
}
.card:hover > .school .course {
  font-weight: 600;
  font-size: 20px;
  line-height: 30px;
  width: 150px;
  color: #5671a6;
}
/* media queries */
@media only screen and (max-width: 600px) {
  .edu-card {
    flex-direction: column;
  }
  .card {
    width: 100%;
  }
}
</style>
