<template>
  <div class="work">
    <div class="work-card">
      <div class="card">
        <div class="jobs">
          <p class="job">Intern(web developer)</p>
          <p class="office">Hiit place</p>
        </div>
        <div class="date">
          <i><img src="../../../public/images/calendar.svg" alt="" /></i>
          <p>2020-2021</p>
        </div>
      </div>
      <div class="card">
        <div class="jobs">
          <p class="job">Intern(frontend web developer)</p>
          <p class="office">Techvibes</p>
        </div>
        <div class="date">
          <i><img src="../../../public/images/calendar.svg" alt="" /></i>
          <p>2022-2023</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.work-card {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 10px;
  gap: 5px;
  margin-top: 2rem;
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
.card .jobs {
  gap: 29px;
  width: 100%;
  height: 98px;
}
.card .jobs .job {
  width: 73px;
  height: 42px;
  font-weight: 600;
  font-size: 14px;
  line-height: 21px;
  margin-bottom: 3rem;
  color: #383838;
  transition: 0.25s;
}
.office {
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
  /* transform: translateY(0.6em); */
  height: 0;
}
.card:hover > .jobs .job {
  font-weight: 600;
  font-size: 20px;
  line-height: 30px;

  color: #5671a6;
}
/* media queries */
</style>
