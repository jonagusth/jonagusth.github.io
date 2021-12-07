<template>
  <div id="lotr">
    <div class="row align-items-center p-3">
      <div class="col-md-6">
        <img src="../assets/LOTR/lotr_logo.png" class="img-fluid" />
      </div>
      <div class="col-md-6">
        <h2>The Lord of the Rings</h2>
        <p>Social Graphs Final project</p>
      </div>
    </div>
    <div class="row align-items-center p-3">
      <div class="col-md-12">
        <h2>The project</h2>
      </div>
      <div class="col-md-12">
        <div class="embed-responsive embed-responsive-1by1">
          <iframe
            class="embed-responsive-item"
            src="LortNetwork.html"
            width="610px"
            height="810px"
          ></iframe>
        </div>
      </div>
      <div class="col-md-12">
        <p>
          This project will investigate connections between characters of the
          Lord of the Rings trilogy.
          <span style="font-weight: bold; color: red"
            >BÆTA EITTHVERJU VIÐ HÉR</span
          >
        </p>
      </div>
    </div>
  </div>
  <div class="row align-items-center p-3">
    <div class="col-md-12">
      <h2>The data</h2>
    </div>
    <div class="col-md-12">
      <img src="../assets/LOTR/placeholder.png" class="img-fluid" />
    </div>
    <div class="col-md-12">
      <p>
        This project uses 3 data sources, where each data source is used to
        perform different analysis.
      </p>
      <h4>Fandom Wiki</h4>
      <p>
        The
        <a href="https://lotr.fandom.com/wiki/Main_Page"
          >Lord of the Rings fandom wiki</a
        >
        is a community driven wiki page, focused on the Lord of the rings
        thematic universe. From this site, lists of characters ,appearing in
        each of the thee movies, were collected. Using this list of characters ,
        the wiki page for every character appearing in the movies were
        collected. Each wiki page contains refrences to other characters. In total
        121 wiki pages were collected, amounting to 1,24MB of data.
      </p>
      <p>
        This data was used to generate a network of the characters. Each
        character is modeled as a node in the network, and each refrence is
        modeled as a link in the network. The network constructed has 121 nodes
        and 710 nodes.
      </p>
      <h4>The Books</h4>
      <p>The books were used as a data source yes</p>

      <h4>The movie scripts (Transcripts)</h4>
      <p>
        Transcripts of the three movies were used a data sources as well. As the transcripts specify
        very well which character is saying what, they were used to perform sentimental analysis for major
        characters, races and cultures. The transcripts were also used to generate word clouds of frequently 
        used words in the films.

      </p>
    </div>
  </div>
  <div class="row align-items-center p-3">
    <div class="col-md-12">
      <h2>The network</h2>
    </div>
    <div class="col-md-12">
      <img src="../assets/LOTR/placeholder.png" class="img-fluid" />
    </div>
    <div class="col-md-12">
      <h4>Tools used</h4>
      <p>
        To model the network, the python package <a href="https://networkx.org/">Networkx</a> was used.
        This package offers many functionaniltie to analyze the network. To visualize the network, <a href="https://github.com/bhargavchippada/forceatlas2">Force atlas 2</a>
        was use to set the positions of the nodes and <a href="http://docs.bokeh.org/en/latest/">bokeh</a> was used to generate an interactive visualisation of the network.
      
      </p>
      <h4>Statistics</h4>
      <p>Once the network was constructed, some general statistics were extracted. The constructed network
        has 121 nodes, with 710 edges. 
      </p>
    </div>
  </div>
  <div class="row align-items-center p-3">
    <div class="col-md-12">
      <h2>A title for a chapter</h2>
    </div>
    <div class="col-md-12">
      <div
        id="carouselExampleIndicators"
        class="carousel carousel-dark slide"
        data-bs-ride="carousel"
      >
        <div class="carousel-indicators">
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="0"
            class="active"
            aria-current="true"
            aria-label="Slide 1"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="1"
            aria-label="Slide 2"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="2"
            aria-label="Slide 3"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="3"
            aria-label="Slide 4"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="4"
            aria-label="Slide 5"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="5"
            aria-label="Slide 6"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="6"
            aria-label="Slide 7"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="7"
            aria-label="Slide 8"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="8"
            aria-label="Slide 9"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="9"
            aria-label="Slide 10"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="10"
            aria-label="Slide 11"
          ></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img
              src="../assets/LOTR/characterWordClouds/aragorn.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/boromir.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/frodo.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/gandalf.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/gimli.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/gollum.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/legolas.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/merry.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/pippin.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/sam.png"
              class="d-block w-100"
            />
          </div>
          <div class="carousel-item">
            <img
              src="../assets/LOTR/characterWordClouds/saruman.png"
              class="d-block w-100"
            />
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </div>
  <div class="row align-items-center p-3">
    <div class="col-md-12">
      <h2>A title for a chapter</h2>
    </div>
    <div class="col-md-12">
      <img src="../assets/LOTR/placeholder.png" class="img-fluid" />
    </div>
    <div class="col-md-12">
      <p>
        A nice text describing the picture. A nice text describing the picture.A
        nice text describing the picture.A nice text describing the picture.A
        nice text describing the picture.A nice text describing the picture.A
        nice text describing the picture.A nice text describing the picture.A
        nice text describing the picture.A nice text describing the picture.A
        nice text describing the picture.A nice text describing the picture.A
        nice text describing the picture.A nice text describing the picture.A
        nice text desc ribing the picture.A nice text describing the picture.A
        nice text describing the pictu re.A nice text describing the picture.
      </p>
    </div>
  </div>

  <div id="about">
    <div class="row">
      <div class="col-4">
        <img
          src="../assets/LOTR/anton.jpg"
          class="img-fluid"
          alt="Responsive image"
        />
        <p class="p-3">
          Anton Freyr Arnarsson
          <br />
          s202443
        </p>
      </div>
      <div class="col-4">
        <img
          src="../assets/berglind.jpg"
          class="img-fluid"
          alt="Responsive image"
        />
        <p class="p-3">
          Berglind Lilja Björnsdóttir
          <br />
          S202073
        </p>
      </div>
      <div class="col-4">
        <img src="../assets/jon.jpg" class="img-fluid" alt="Responsive image" />
        <p class="p-3">
          Jón Ágúst Hannesson
          <br />
          s202057
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LordOfTheRings",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#lotr {
  /* background-color: rgb(255, 255, 255); */
  /* height: 700px; */
  width: 100%;
  padding: 30px 200px 30px 200px;
}

#about {
  /* height: 700px; */
  width: 100%;
  height: 100%;
}

.li .borderless {
  border-top: 0 none;
  border-bottom: 0 none;
}
</style>
