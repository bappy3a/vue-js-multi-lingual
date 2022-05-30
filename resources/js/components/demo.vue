<template>
<div>

    <h1>{{ $t('hello') }}</h1>
</div>

</template>

<script>
export default {
    methods:{
        // changeLanguage(obj){
        //     localStorage.setItem('language',obj.target.value)
        // }]
        changeLanguage(obj){
            const token = "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJhdWQiOiIxNSIsImp0aSI6IjA3M2NkNDYwMDI2MzI0ZDA1MzdmOWFhOWU3OWZiZTNlMzJiOWQ5MDYzM2U1NmUxMjQyNDliMDA5M2Q2OTZmMmE2OGUzZDYyZmI4OTkxYzljIiwiaWF0IjoxNjQzMTk2MzIwLjE0MTc1OCwibmJmIjoxNjQzMTk2MzIwLjE0MTc2NSwiZXhwIjoxNjc0NzMyMzIwLjExODkyMiwic3ViIjoiOSIsInNjb3BlcyI6W119.mNjpM61GapfIiAK3NrVhgGGL0CHPS4H21cEMYxZ37FLnWuzaW3p8iEHRWLjHaaHp1udq9maL7JQA4EHbRc-U_sl5opfvZJfZRouAur9t0Eu5m3lHTZigCbu28BZ8HMu0jtjZFTa2Dt8OX8I8sbmkDSkJRo8LoUuXa8RKAdKEl9dmoXwzoSrYc51kzYDAwJqmwWPsA6-PbIEAH-CQnsCuhgJDzGtzVMmoalKKfIW8IQ95RHBdjpzmsCj6Va8UEd14HZ5mPFnl3TcVgl53JjuISXWSfK8JoJrBFYgNycDh02K5Fyn_zHQw-6gdZMPc1jbuRWtOyiSDBI5LOftefYgl7rYGBgeb_0hXyX5IVummveu8anNC4LV24dBMuR7PsdJt1hOa0eb9QuMyRjBujyHbdvi4f1M5AZi4q44K-LIl61Kvp3ls3yPYaHkpmy7d-hV9mpzCBW-PEhgYzR97_aKGO1jLT-6q5Z38dRi5NA71M5kiz4-RXiA-TcLfLbTgKJTZeM1xq7sAbc4wTvq8ZNjsCUh_p621gqa8oIs5wcsD13fdgOJi7fW4rowEDmwvkkg2sXi-1vKEV_Me3EyMyP6JXpJzHkxawBFw6-OY0yjXcFlat4OkNv1DSJ_sROKaWY6032LhlskesxlENhfcvYeHbhpASkYJHFBKD1VhgmgrUPk";
      axios.post("https://dev.hishabee.business/api/V2/online-shop/publish?shop_id=18",
        {
            headers: {"Authorization" : `Bearer ${token}`}

        })
        .then((response) => {
            console.log(response.data);
        })
        .catch((e) => {
          console.log(e);
        });
        }
    }
}
</script>
