<template>
  <div id="lotr">
    <div class="row align-items-center p-3">
      <div class="col-md-2"></div>
      <div class="col-md-8">
        <div class="row align-items-center p-3">
          <div class="col-md-6">
            <img src="../assets/LOTR/lotr_logo.png" class="img-fluid" />
          </div>
          <div class="col-md-6">
            <h2 class="display-4">The Lord of the Rings</h2>
            <p>Social Graphs Final project</p>
          </div>
        </div>
        <div class="row align-items-center p-3">
          <div class="col-md-12">
            <h2 class="display-4">The project</h2>
          </div>
          <div class="col-md-12">
            <p>
              In this project the Lord of the Rings thematic universe will be
              investigated. In Lord of the rings there are many characters of
              very distinct and diverse races which interact with each other on
              all kinds of levels, using network analysis.
            </p>
            <p>
              For example, the relationships between races and the cultures
              within races will be investigated. As an example, the differences
              between Rohirrim and The men of Gondor. Alongside this,
              sentimental analysis and various natural language analysis will be
              performed.
            </p>
          </div>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <h2 class="display-4">The data</h2>
          <p>
            Our main dataset was the Lord of the rings fandom wiki. The three
            Lord of the rings books: "The fellowship of the Ring", "The two
            towers", "The return of the King" and their movie counterparts were
            also used to deepen the analysis and to introduce temporal analysis.
          </p>
        </div>
        <div class="col-md-6">
          <h4>Fandom Wiki</h4>
          <p>
            The
            <a href="https://lotr.fandom.com/wiki/Main_Page"
              >Lord of the Rings fandom wiki</a
            >
            is a community driven wiki page, focused on the Lord of the rings
            thematic universe. From this site, lists of characters ,appearing in
            each of the thee movies, were collected. Using this list of
            characters , the wiki page for every character appearing in the
            movies were collected. Each wiki page contains refrences to other
            characters. In total 121 wiki pages were collected, amounting to
            1,24MB of data.
          </p>
          <p>
            This data was used to generate a network of the characters. Each
            character is modeled as a node in the network, and each refrence is
            modeled as a link in the network. The network constructed has 121
            nodes and 710 nodes.
          </p>
        </div>
        <div class="col-md-6">
          <figure>
            <img src="../assets/LOTR/fandom.png" class="img-fluid" />
            <figcaption>The fandom page for Aragorn</figcaption>
          </figure>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <h4>The Books</h4>
          <p>
            The text files for all the Lord of the Rings books where downloaded
            from the following
            <a href="http://www.glozman.com/textpages.html">web site.</a>
            The books are used to perform natural language processing. They will
            be used to analyze the sentiment for each chapter in the books, the
            distribution of interesting words throughout the books and generate
            word clouds of frequently used words, among other things.
          </p>
        </div>
        <div class="col-md-6">
          <h4>The movie scripts (Transcripts)</h4>

          <p>
            Transcripts of the three movies were used a data sources as well. As
            the transcripts specify very well which character is saying what,
            they were used to perform sentimental analysis for major characters,
            races and cultures. The transcripts were also used to generate word
            clouds of frequently used words in the films.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <h2 class="display-4">The network</h2>
        </div>
        <!-- <div class="col-md-12">
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
            The following plot is an interactive visualisation of the network.
            The network visualized is the undirected variant of the giant
            component of the entire network. The sizes of the nodes represent
            their degree and the nodes are colored by their community. Hovering
            over a displays the name of the character, their degree, race,
            cultures and community.
          </p>
        </div> -->
        <div class="col-md-12">
          <h4>Tools used</h4>
          <p>
            To model the network, the python package
            <a href="https://networkx.org/">Networkx</a> was used. This package
            offers many functionaniltie to analyze the network. To visualize the
            network,
            <a href="https://github.com/bhargavchippada/forceatlas2"
              >Force atlas 2</a
            >
            was use to set the positions of the nodes and
            <a href="http://docs.bokeh.org/en/latest/">bokeh</a> was used to
            generate an interactive visualisation of the network.
          </p>
          <h4>Statistics</h4>
          <p>
            Once the network was constructed, some general statistics were
            extracted. The constructed network has 121 nodes, with 710 edges.
          </p>
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
            The following plot is an interactive visualisation of the network.
            The network visualized is the undirected variant of the giant
            component of the entire network. The sizes of the nodes represent
            their degree and the nodes are colored by their community. Hovering
            over a displays the name of the character, their degree, race,
            cultures and community.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <h4>Degree distribution</h4>
          <p>
            The following graphs show the degree distribution of the network.
          </p>
          <p>
            The first graph shows the distribution of in degrees in the network
            or how many times each character is refrenced by another character.
            The distribution shows that most characters in the network have a
            low in degree, between 0 and 10. A few characters have very high in
            degree, more than 40. As there are a lot of characters in the Lord
            of the rings, minor characters tend to have smaller wiki pages, with
            few refrences. Those refrences tend to be to major characters in the
            story.
          </p>
          <p>
            The second graph shows the distribution of out degrees in the
            network. It can be seen that no characters in the network have an
            out degree of 0, or that every character in the network have at
            least one refrence to another character in the network. Similarly to
            the in degree distribution, the out degree distribution shows that
            many characters have a low out degree, and a few characters have a
            high out degree. As major characters in the Lord of the Rings tend
            to have long and detailed wiki pages, they also have many refrences
            to other characters.
          </p>
          <p>
            The third graphs shows the distribution of total degree in the
            network. It follows a similar structure as the earlier two, with
            many characters with low total degree, and a few ones with a high
            total degree.
          </p>
        </div>
        <div class="col-md-6">
          <div
            id="carouselDegree"
            class="carousel carousel-dark slide"
            data-bs-ride="carousel"
          >
            <div class="carousel-indicators">
              <button
                type="button"
                data-bs-target="#carouselDegree"
                data-bs-slide-to="0"
                class="active"
                aria-current="true"
                aria-label="Slide 1"
              ></button>
              <button
                type="button"
                data-bs-target="#carouselDegree"
                data-bs-slide-to="1"
                aria-label="Slide 2"
              ></button>
              <button
                type="button"
                data-bs-target="#carouselDegree"
                data-bs-slide-to="2"
                aria-label="Slide 3"
              ></button>
            </div>
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img
                  src="../assets/LOTR/network/indegrees.png"
                  class="d-block w-100"
                />
              </div>
              <div class="carousel-item">
                <img
                  src="../assets/LOTR/network/outDegrees.png"
                  class="d-block w-100"
                />
              </div>
              <div class="carousel-item">
                <img
                  src="../assets/LOTR/network/totalDegrees.png"
                  class="d-block w-100"
                />
              </div>
            </div>
            <button
              class="carousel-control-prev"
              type="button"
              data-bs-target="#carouselDegree"
              data-bs-slide="prev"
            >
              <span
                class="carousel-control-prev-icon"
                aria-hidden="true"
              ></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button
              class="carousel-control-next"
              type="button"
              data-bs-target="#carouselDegree"
              data-bs-slide="next"
            >
              <span
                class="carousel-control-next-icon"
                aria-hidden="true"
              ></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <table class="table">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">In degree</th>
                <th scope="col">Out degree</th>
                <th scope="col">Total degree</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row">1</th>
                <td>Saruman - 44</td>
                <td>Aragorn - 33</td>
                <td>Aragorn - 67</td>
              </tr>
              <tr>
                <th scope="row">2</th>
                <td>Sauron - 41</td>
                <td>Gandalf - 29</td>
                <td>Frodo - 66</td>
              </tr>
              <tr>
                <th scope="row">3</th>
                <td>Frodo - 41</td>
                <td>Frodo - 25</td>
                <td>Saruman - 60</td>
              </tr>
              <tr>
                <th scope="row">4</th>
                <td>Aragorn - 34</td>
                <td>Galadriel - 18</td>
                <td>Gandalf - 59</td>
              </tr>
              <tr>
                <th scope="row">5</th>
                <td>Gandalf - 30</td>
                <td>Éomer - 17</td>
                <td>Sauron - 55</td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="col-md-6">
          <h4>Top connected characters</h4>
          <p>
            It might not be a big suprise that the top connected characters in
            the network are major characters in the story.
          </p>
          <p>
            Saruman and Sauron top the charts for the in degree. These two are
            the main antoganists in the story. Many minor characters refrence
            these on their wiki pages. Frodo has the equal amount of refrences
            to Sauron. He is of course the carrier of the ring and arguably the
            main character of the story, so it is no suprise he ranks highly.
          </p>
          <p>
            Aragorn is the highest ranking character, in regard to the out
            degree. Throughout the story he interacts with many different
            characters.
          </p>
        </div>
      </div>

      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <h4>Communities</h4>
          <p>texti eða tafla</p>
        </div>
        <div class="col-md-6">
          <p>texti eða tabbbbla</p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <img src="../assets/LOTR/network/culture.png" class="img-fluid" />
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <h4>Distribution of cultures</h4>
          <p>
            In the following graph the distribution of cultures can be seen. The
            top cultures in the network are: 'The shire', 'Rohirrim' and 'The
            men of Gondor'. As the story starts in the shire, many characters
            appear early on that have 'the shire' as their culture. The latter
            two are the cultures of the two largest group of men in the stories,
            so it is no suprise they are so populated. As can be seen is this
            graph, many cultures are represented by one character in the
            network.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <h2 class="display-4">The books</h2>
        </div>

        <div class="col-md-12">
          <p>
            The following section covers the analysis conducted from the three
            Lord of the Rings Books. This section covers general statistics,
            temporal sentiment analysis, different types of word clouds and
            lexical dispersion.
          </p>
        </div>
        <div class="col-md-12">
          <img src="../assets/LOTR/books/stats.png" class="img-fluid" />
        </div>
      </div>
      <div class="row align-items-center p-3">
        <h4>Lexical Dispersion Plot</h4>
        <p>
          An interesting part of text analysis is a lexical dispersion. This
          plot shows how a list of words of interests appear in the text over
          the three books. The blue lines distinguish between books.
        </p>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-4">
          From this plot there are some interesting findings:
          <ul>
            <li>Frodo is definitely the main character in the first book.</li>
            <li>
              In The Two Tower and The Return of the King, Frodo and Sam are
              both is significant in the second half of the books. When one is
              spoken about, the other is not far away.
            </li>
            <li>Gollum and the precious are often mentioned together.</li>
            <li>
              The words "dark" and "ring" are frequently mentioned over the
              three books.
            </li>
            <li>
              Since the three book are all the same story, there are few words
              bound to one book.
            </li>
          </ul>
        </div>
        <div class="col-md-8">
          <img src="../assets/LOTR/books/lex.png" class="img-fluid" />
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <img src="../assets/LOTR/books/wordFreq.png" class="img-fluid" />
        </div>
        <div class="col-md-6">
          <p>
            The next analysis for the books is to find term frequency. The plan
            is to find the most common words for all the books, and for each
            book.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <p>
            Now for the term frequency for all the whole books. The term
            frequency can be viewed in the following word cloud.
          </p>
        </div>
        <div class="col-md-6">
          <img src="../assets/LOTR/books/allBooks.png" class="img-fluid" />
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <p>
            The following word clouds highlight the most important words that
            appear in the books. These word were generated using TC-IDF.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-4">
          <figure>
            <img src="../assets/LOTR/books/fotrBook.png" class="img-fluid" />
            <figcaption>The fellowship of the Ring</figcaption>
          </figure>
        </div>
        <div class="col-md-4">
          <figure>
            <img src="../assets/LOTR/books/ttBook.png" class="img-fluid" />
            <figcaption>The fellowship of the Ring</figcaption>
          </figure>
        </div>
        <div class="col-md-4">
          <figure>
            <img src="../assets/LOTR/books/rotkBook.png" class="img-fluid" />
            <figcaption>The fellowship of the Ring</figcaption>
          </figure>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-6">
          <img
            src="../assets/LOTR/books/sentiment_all_books.png"
            class="img-fluid"
          />
        </div>
        <div class="col-md-6">
          <p>
            In this section a temporal sentiment analysis will be made. First a
            sentiment score for each book, and later a sentiment score for each
            chapter, which will show the development of sentiment over the book
            series. A sentiment plot shows different sentiment scores for each
            chapter, depending on how positive or negative the chapter is.
          </p>
          <p>
            When calculating sentiment score, it was decided to use a frequency
            distribution of a certain text. The sentiment score for each word
            was found, and then multiplied with it's frequency in the text. The
            average score is then found with total score of all words, divided
            by number of words with score in text. Since not all words have a
            sentiment score, words like "Frodo" are neutral and therefore do not
            affect the analysis.
          </p>
          <p>
            In this sentimental plot, we see how the sentimental score goes down
            between books. This is understandable as the story gets darker and
            darker. But even though the book's sentiment score goes down, it is
            on average always above 0, so it can be said that the Lord of the
            Rings book series is a positive one.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <img src="../assets/LOTR/books/setnChapter.png" class="img-fluid" />
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <p>
            In this sentimental plot, we see how chapters differ in average
            sentiment score. Chapter 1 (A Long-expected Party) is quite happy
            while chapter 17 (The Bridge of Khazad-dum) is the most negative
            chapter of the series. Here our main characters are inside Moria,
            and Gandalf memorably falls of the bridge, after Balrog snatched him
            down with his fire whip. Quite dark stuff. It is also noticable that
            the difference between the two last chapters is very positive. The
            black vertical line is on 0. Chapters above are positive, chapters
            below are negative.
          </p>
        </div>
      </div>
      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <h2 class="display-4">The movies</h2>
        </div>
        <div class="col-md-12">
          <div class="row align-items-center p-3">
            <div class="col-md-4">
              <figure>
                <img
                  src="../assets/LOTR/movies/fellowship.jpg"
                  class="img-fluid"
                />
                <figcaption>The fellowship of the Ring</figcaption>
              </figure>
            </div>
            <div class="col-md-4">
              <figure>
                <img
                  src="../assets/LOTR/movies/two_towers.jpg"
                  class="img-fluid"
                />
                <figcaption>The fellowship of the Ring</figcaption>
              </figure>
            </div>
            <div class="col-md-4">
              <figure>
                <img
                  src="../assets/LOTR/movies/return_of_the_king.jpg"
                  class="img-fluid"
                />
                <figcaption>The fellowship of the Ring</figcaption>
              </figure>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <p>
            The following chapter covers the analysis conducted on the
            transcripts of the three Lord of the Rings movies. This chapter
            covers language processing of the three Lord of the Rings movies
            through word clouds for each movie and a sentiment analysis of
            characters, races and cultures of men. Transcripts are ideal
            language processing and for a sentiment analysis since they display
            very clearly which character in the movies says what. Let's take for
            example: Gandalf: If you’re referring to the incident with the
            dragon, I was barely involved. All I did was give your uncle a
            little nudge out of the door. Frodo: Whatever you did, you’ve been
            officially labeled a disturber of the peace. Gandalf: Oh really?
            this has been processed into: <br />
            "frodo baggins": [" Whatever you did, you’ve been officially labeled
            a disturber of the peace. "]
            <br />
            "gandalf": ["If you’re referring to the incident with the dragon, I
            was barely involved. All I did was give your uncle a little nudge
            out of the door.", "Oh really?"]
            <br />
            Which can then be used for the analysis
          </p>
        </div>
        <div class="col-md-12">
          <h4>Language Processing</h4>
        </div>
        <div class="col-md-12">
          <p>
            From the transcripts the the dialogue of the major characters could
            be analyzed. In this section wordclouds of frequent words for the
            major characters will be generated. Word clouds for the films in
            general will also be generated.
          </p>
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
              <span
                class="carousel-control-prev-icon"
                aria-hidden="true"
              ></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button
              class="carousel-control-next"
              type="button"
              data-bs-target="#carouselExampleIndicators"
              data-bs-slide="next"
            >
              <span
                class="carousel-control-next-icon"
                aria-hidden="true"
              ></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </div>
        <div class="col-md-12">
          <p>
            These are the word clouds for major characters, based on term count
            from their movie dialogue. The frequency of the words is represented
            by their size in the word cloud. Some interesting patterns can be
            seen in the word clouds. Most of the characters frequently mention
            other characters, whereas Frodo is mentioned often by most of the
            characters. Merry and Pippin mention each other very frequently,
            which is understandable as they two do almost everything together
            throughout the movies. Gollum's word cloud is interesting as his
            dialogue is very different from that of the other major characters.
            Gollum's most frequent word is Sméagol, which of course is one of
            his two personalities. These personalities have a dialogue between
            themselves in the films. The words master (his name for Frodo) and
            precious (the ring), also appears frequently in his dialogue. Next,
            wordclouds based on the films themselves will be generated.
          </p>
        </div>
        <div class="col-md-12">
          <img
            src="../assets/LOTR/movies/all_movies_cloud.png"
            class="img-fluid"
          />
        </div>
        <div class="col-md-12">
          <p>
            This word cloud is a collection of the most frequent words used
            througout all the three movies. From the word cloud it can be seen
            that the 'ring' and 'Frodo' are the top things on characters minds,
            as they are mentioned most frequently throughout the movies. Next,
            word clouds will be generated for each movie. To generate these
            wordclouds tc-idf will be used. Tc-idf highlights the importance of
            words for each film, so words that are bigger ,in the rendered word
            cloud, hold more importance/are more distinctive for that movie.
          </p>
        </div>
        <div class="col-md-12">
          <div class="row align-items-center p-3">
            <div class="col-md-4">
              <figure>
                <img
                  src="../assets/LOTR/movies/fellowship_movie_cloud.png"
                  class="img-fluid"
                />
                <figcaption>The fellowship of the Ring</figcaption>
              </figure>
            </div>
            <div class="col-md-4">
              <figure>
                <img
                  src="../assets/LOTR/movies/two_towers_move_cloud.png"
                  class="img-fluid"
                />
                <figcaption>The fellowship of the Ring</figcaption>
              </figure>
            </div>
            <div class="col-md-4">
              <figure>
                <img
                  src="../assets/LOTR/movies/return_movie_cloud.png"
                  class="img-fluid"
                />
                <figcaption>The fellowship of the Ring</figcaption>
              </figure>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <p>
            For the first movie, The fellowship of the ring, the most important
            words are 'Strider' (an nickname for Aragorn) and Bilbo. Overall the
            word cloud is quite possitive, with words like 'Hello','goodnight'
            and 'tea' appearing prominantly. The first film start of quite happy
            and without much hardship and this is reflected in the word cloud.
            The word cloud for the second film, The two Towers, is not as
            possitive as the first film. Words like 'war', 'hopeless' and
            'danger' can be seen. The most important words are 'precious',
            'Sméagol', 'Ent' and 'Théoden'. Gollum appears first in this film so
            his name and the word 'precious' are highlighted here. The word
            cloud for the third film, Return of the King, higlithts 'Sméagol',
            'Tirith', 'Denethor' and 'war'. In the third the battle for Minas
            Tirith takes place, whose king is Denethor. This word cloud, like
            the one for The two Towers, is quite negative overall.
          </p>
        </div>
        <div class="col-md-12">
          <h4>Sentiment Analysis</h4>
        </div>
        <div class="col-md-12">
          <p>
            Sentiment Analysis is a good tool for analysing the mood of the
            movies. From the transcripts the sentiment of characters, races and
            cultures can be calculated. Let's start by defining the happiest and
            saddest characters.
          </p>
        </div>
        <div class="col-md-12">
          <div class="row align-items-center p-3">
            <div class="col-md-6">
              <figure>
                <img
                  src="../assets/LOTR/movies/happiest_characters.png"
                  class="img-fluid"
                />
              </figure>
            </div>
            <div class="col-md-6">
              <figure>
                <img
                  src="../assets/LOTR/movies/saddest_characters.png"
                  class="img-fluid"
                />
              </figure>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <p>
            It comes a no surprise that many of the happiest characters are
            Hobbits. Hobbits are shy creature but yet capable of amazing things.
            They enjoy farmin, food, parties and presetns. They are friendly,
            happy creatures and therefore it comes as no surprise that they are
            the happiest of all. The list of saddest characters includes
            Gothmog, a corrupt being whose weapon of choice is a fiery whip,
            Black Uruks, a dark wizard and The Ring itself. It also includes
            Léowyn, a Rohirrin woman who disguises herself as a soilder and
            fought in the Battle of the Pelennor Fields.
          </p>
        </div>
        <div class="row align-items-center p-3">
          <div class="col-md-8">
            <img
              src="../assets/LOTR/movies/movie_sentiment_characters.png"
              class="img-fluid"
            />
          </div>
          <div class="col-md-4">
            <p>
              Merry, an intelligent hobbit with a fondness for boats and ponies,
              is the happiest of the main characters. This fits the movies well
              since Merry is known for thinking and talking about food even in
              the most dangerous situations. Merries knack for complementing
              others, especially his dear friend Pippin also has an affect of
              his sentiment score. Boromir, a warrior of Gondor, has the second
              highest sentiment but for a very different reason than Merry. He
              does not speak about food, instead he uses words like faith, glory
              and kings which influence his sentiment score for the better.
            </p>
          </div>
        </div>
        <div class="row align-items-center p-3">
          <div class="col-md-6">
            <img
              src="../assets/LOTR/movies/movie_sentiment_races.png"
              class="img-fluid"
            />
            <p>
              All three Lord of the Rings movies have an overwhelming amount of
              hardship versus happiness. It therefore does not come as a
              surprise that the sentiments of all races is quite low. There
              seems to be little difference between the highest and lowest
              sentiments of races. This can be explained by the fact that the
              precence of hardship and pain is mirrored in both the sentiment of
              the cause, for example Orks or Uruk-hai, but also in the races who
              suffer, such as hobbits and men (in some cases, not all).
            </p>
          </div>
          <div class="col-md-6">
            <img
              src="../assets/LOTR/movies/movie_sentiment_men.png"
              class="img-fluid"
            />
            <p>
              Taking a look at the sentimen scores of the most common cultures
              of men it can be seen that the scores are very similar. The house
              of Húrin and the men of Gondor have slightly higher scores.
              Boromin, main character with the second highest sentiment score
              and the fourth highest sentiment score of any character, is a
              member of bith of these cultures which might explain the slight
              increas in positive
            </p>
          </div>
        </div>
      </div>

      <div class="row align-items-center p-3">
        <div class="col-md-12">
          <h2 class="display-4">Comparisons - Books and Movies</h2>
          <p>
            Having analyzed the three Lord of the Rings books and their movie
            counterparts it is worthwile to compare the two and take a look a
            where the different formats of portraying the stories are similar
            and where they differ.
          </p>
        </div>
        <div class="col-md-12">
          <h4>Language processing</h4>
        </div>
        <div class="col-md-12">
          <div class="row align-items-center p-3">
            <div class="col-md-12">
              <div class="row align-items-center p-3">
                <div class="col-md-4">
                  <figure>
                    <img
                      src="../assets/LOTR/books/fotrBook.png"
                      class="img-fluid"
                    />
                    <figcaption>The fellowship of the Ring</figcaption>
                  </figure>
                </div>
                <div class="col-md-4">
                  <figure>
                    <img
                      src="../assets/LOTR/books/ttBook.png"
                      class="img-fluid"
                    />
                    <figcaption>The two Towers</figcaption>
                  </figure>
                </div>
                <div class="col-md-4">
                  <figure>
                    <img
                      src="../assets/LOTR/books/rotkBook.png"
                      class="img-fluid"
                    />
                    <figcaption>Return of the King</figcaption>
                  </figure>
                </div>
              </div>
            </div>
            <div class="col-md-12">
              <div class="row align-items-center p-3">
                <div class="col-md-4">
                  <figure>
                    <img
                      src="../assets/LOTR/movies/fellowship_movie_cloud.png"
                      class="img-fluid"
                    />
                    <figcaption>The fellowship of the Ring</figcaption>
                  </figure>
                </div>
                <div class="col-md-4">
                  <figure>
                    <img
                      src="../assets/LOTR/movies/two_towers_move_cloud.png"
                      class="img-fluid"
                    />
                    <figcaption>The two Towers</figcaption>
                  </figure>
                </div>
                <div class="col-md-4">
                  <figure>
                    <img
                      src="../assets/LOTR/movies/return_movie_cloud.png"
                      class="img-fluid"
                    />
                    <figcaption>Return of the King</figcaption>
                  </figure>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <p>
            There seems to be little resembelence between the word clouds of the
            books and movies. For The fellowship of the Ring the book data
            highlights "pony" and characters such as Barliman Butterbur, an
            inn-keeper from Bree, and Goldberry, the wife of Tom Bombdil in the
            Old Forest. However in the movies Strider, better known as Aragorn,
            Bilbo Baggins and tea are highlighted. One point of resembelence is
            that the importans of ents, specifically Treebeard, and trees in
            general seems to be present in both the books and movie adaptations
            of the Two Towers.
          </p>
        </div>
        <div class="col-md-12">
          <h4>Sentiment analysis</h4>
        </div>
        <div class="col-md-12">
          <div class="row align-items-center p-3">
            <div class="col-md-6">
              <figure>
                <img
                  src="../assets/LOTR/books/sentiment_all_books.png"
                  class="img-fluid"
                />
              </figure>
            </div>
            <div class="col-md-6">
              <figure>
                <img
                  src="../assets/LOTR/movies/all_movies_sentiment.png"
                  class="img-fluid"
                />
              </figure>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <p>
            It is clear that in both movies and books the sentiment score gets
            lower with each addition to the saga. However the sentiment score in
            the books starts out higher than in the movies and also has a higher
            value in the second book compared to the second movie. Both books
            and movies have a very similar score in the last additions. It can
            therefore be concluded that although both books and movies follow
            the same pattern there is a bigger contrast between the start end
            end point of the saga in the books rather than movies.
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
            <img
              src="../assets/jon.jpg"
              class="img-fluid"
              alt="Responsive image"
            />
            <p class="p-3">
              Jón Ágúst Hannesson
              <br />
              s202057
            </p>
          </div>
        </div>
        <div class="row align-items-center p3">
          <div class="col-md-12">
            <h4>Want to learn more about the project?</h4>
            <p>
              The source code for this project can be found on
              <a
                href="https://github.com/BerglindLilja/DataQueens/tree/main/Project"
                >github</a
              >
              and an jupyter notebook going in to further detail can be viewed
              <a
                href="https://nbviewer.org/github/BerglindLilja/DataQueens/blob/main/Project/Explainer_notebook.ipynb"
                >here.</a
              >
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-2"></div>
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
figcaption {
  font-weight: bold;
}
</style>
