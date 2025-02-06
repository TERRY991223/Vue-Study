<template >
    <section id="about" class="container">
        <h1>About</h1>
        <div class="row gx-5">
            <figure class="col-md-6">
                <img src="../assets/images/profile.jpg">
                <figcaption>About Terry</figcaption>
            </figure>
            <p class="col-md-6">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nihil suscipit in ut fuga reiciendis tenetur voluptate, deserunt modi velit iste reprehenderit possimus aut eos quidem facilis odio voluptatem ad necessitatibus?</p>
        </div>

        <article class="row mt-5">
            <h2>Skills</h2>
            <dl>
                <dt class="lead">HTML</dt>
                <dd>
                <div 
                    class="progress" 
                    role="progressbar"
                >
                    <div class="progress-bar" style="width: 90%"></div>
                </div>
                </dd>
                <dt class="lead">CSS</dt>  
                <dd>
                <div 
                    class="progress" 
                    role="progressbar"
                >
                    <div class="progress-bar" style="width: 80%"></div>
                </div>
                </dd>
                <dt class="lead">JavaScript</dt>
                <dd>
                <div 
                    class="progress" 
                    role="progressbar"
                >
                    <div class="progress-bar" style="width: 50%"></div>
                </div>
                </dd>
                <dt class="lead">Vue</dt>
                <dd>
                <div 
                    class="progress" 
                    role="progressbar"
                >
                    <div class="progress-bar" style="width: 75%"></div>
                </div>
                </dd>
            </dl>
        </article>
    </section>
</template>
<script>
    const skills =[
    {name:'HTML', point:'90%'},
    {name:'CSS', point:'80%'},
    {name:'JAVASCRIPT', point:'70%'},
    {name:'VUE', point:'75%'},
    ]
    

</script>
<style lang="scss">
    figure img {
        width: 100%;
    }
</style>