<template>
<nav
  id="monarch-navbar"
  class="navbar navbar-inverse navbar-fixed-top"
  role="navigation">
  <div class="container-fluid monarch-navbar-container">
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>

      <router-link to="/" class="navbar-brand">
              <img class="branding-logo pull-left"
                   src="/image/logo.png"
                   alt="Monarch Initiative logo"
                   title="Monarch Initiative front page"/>
              <span class="pull-right">Monarch</span>
      </router-link>
    </div>
    <div id="navbar" class="navbar-collapse collapse">
      <ul class="nav navbar-nav">
          <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                  <i class="icon-th-large"></i>Browse <b class="caret"></b>
              </a>
              <ul class="dropdown-menu">
                  <li><router-link to="/disease">Diseases</router-link></li>
                  <li><router-link to="/phenotype">Phenotypes</router-link></li>
                  <li><router-link to="/gene">Genes</router-link></li>
                  <li><router-link to="/model">Models</router-link></li>
              </ul>
          </li>
          <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                  <i class="icon-th-large"></i>Analyze <b class="caret"></b></a>
              <ul class="dropdown-menu">
                  <li><router-link to="/analyze/phenotypes">Phenotypes</router-link></li>
                  <li><router-link to="/annotate/text">Annotate Text</router-link></li>
                  <li><router-link to="/page/exomes">Exomes</router-link></li>
              </ul>
          </li>
          <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                  <i class="icon-th-large"></i>About <b class="caret"></b></a>
              <ul class="dropdown-menu">
                  <li><router-link to="/page/aboutSPA">About Monarch (SPA)</router-link></li>
                  <li><router-link to="/page/about">About Monarch</router-link></li>
                  <li><router-link to="/about/sources">Data Sources</router-link></li>
                  <li><router-link to="/page/releases">Releases</router-link></li>
                  <li><router-link to="/page/team">Monarch Team</router-link></li>
                  <li><router-link to="/page/disclaimer">Monarch Disclaimer</router-link></li>
                  <li role="separator" class="divider"></li>
                  <li><router-link to="/page/services">Monarch Web Services and APIs</router-link></li>
                  <li><a target="_blank" href="https://archive.monarchinitiative.org/latest ">Data Downloads</a></li>
              </ul>
          </li>
          <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                  <i class="icon-th-large"></i>Documentation<b class="caret"></b></a>
              <ul class="dropdown-menu">
                  <li><router-link to="/page/phenogrid">Monarch Phenotype Grid Widget</router-link></li>
                  <li><a target="_blank" href="http://monarch-initiative.blogspot.com/2015/01/how-to-annotate-patients-phenotypic.html">Phenotype Curation Guidelines</a></li>
                  <li><a target="_blank" href="https://github.com/monarch-initiative">GitHub Organization</a></li>
                  <li><a target="_blank" href="https://github.com/obophenotype/upheno">Phenotype Ontologies Project</a></li>
                  <li><router-link to="/page/pubs">Publications</router-link></li>
                  <li><router-link to="/page/links">Link To Us</router-link></li>
              </ul>
          </li>

          <li id="feedback-window-container" class="dropdown">
            <button
              id="feedback-trigger"
              href="#simple-menu"
              data-backdrop="false"
              data-toggle="modal"
              class="btn dropdown-toggle"
              role="button"
              aria-haspopup="true"
              aria-expanded="false">
              Feedback&nbsp;
              <i class="glyphicon glyphicon-pencil" aria-hidden="true"></i>
            </button>
            <ul id="simple-menu" class="dropdown-menu simple-menu modal">
              <li id="feedback-handle" xclass="modal-dialog">
                <div id="feedback-main">
                  <button class="close feedback-close"
                    data-dismiss="modal" xdata-target="#simple-menu">
                    <i class="glyphicon glyphicon-remove-circle" aria-hidden="true"></i>
                  </button>

                  <div class="feedback-drag-instructions">
                      This window may be moved by dragging here
                  </div>
                  <form style="padding:0;">
                    <h5>
                    Specific feedback from users like you is essential to guide future development and improvement of the Monarch experience. We welcome you to answer the questions below and/or contact us via links below.
                    </h5>

                    <div class="form-group">
                      <label for="goal">What did you come to the Monarch site to do?</label>
                      <textarea class="form-control" rows="2" id="feedback-goal"></textarea>
                    </div>

                    <div class="form-group">
                      <label for="improve">What could we improve to make this task easier for you?</label>
                      <textarea class="form-control" rows="2" id="feedback-improve"></textarea>
                    </div>

                    <br/>

                    <div class="form-group form-inline">
                      <div class="checkbox">
                        <label>
                          <input type="checkbox" id="feedback-OKQuote">
                          <span>&nbsp;It is OK to quote my feedback</span>
                        </label>
                      </div>
                    </div>

                    <div class="form-group form-inline">
                      <div class="checkbox">
                        <label>
                          <input type="checkbox" id="feedback-OKFollowup">
                          <span>&nbsp;It is OK to follow up with me about my feedback</span>
                        </label>
                      </div>
                    </div>


                    <div class="form-group form-inline">
                      <label for="feedback-email" style="padding-right:20px;">
                        E-mail (optional)
                      </label>
                      <input class="form-control" style="border:1px solid black;" type="text" id="feedback-email" value="">
                    </div>

                    <div class="form-group">
                      <label for="feedback-additional">Any additional comments?</label>
                      <textarea class="form-control" rows="2" id="feedback-additional"></textarea>
                    </div>

                    <hr style="border:1px solid transparent;margin:5px;padding:0;"/>

                    <div class="form-group">
                      <div style="width:35%;margin:auto;">
                        <input id="feedback-submit-button" class="btn btn-primary btn-sm btn-block" type="button" name="submit" value="Submit Feedback" />
                      </div>
                    </div>
                  </form>

                  <hr style="border-top-color:darkgray;margin:0;margin-top:15px;margin-bottom:0;padding:0;"/>

                  <div class="row">
                    <div class="col-12 text-center">
                      <h5 class="text-center">More Ways to Contact Monarch</h5>
                    </div>
                  </div>
                  <div class="row">
                    <div class="col-xs-3">
                        <a href="https://github.com/monarch-initiative/monarch-app/issues" target="_blank">Issue Tracker</a>
                    </div>
                    <div class="col-xs-3">
                        <a href="mailto:info@monarchinitiative.org" target="_blank">Email Us</a>
                    </div>
                    <div class="col-xs-3">
                        <a href="https://bit.ly/monarchcommunity" target="_blank">Sign Up</a>
                    </div>
                    <div class="col-xs-3">
                        <a href="https://twitter.com/MonarchInit" target="_blank">Follow us on Twitter</a>
                    </div>
                  </div>
                </div>

              </li>
            </ul>
          </li>
      </ul>

      <form
        v-on:submit="searchSubmit"
        id="search_form" class="navbar-right navbar-form searchspace"
          action="/search" role="search">
          <div class="form-group">
            <input id="search" type="text" class="col-xs-8 form-control" placeholder="Search (e.g. Parkinson's)"/>
            <button class="col-xs-4 btn btn-primary nav-search-btn"
                type="submit">Go</button>
          </div>
      </form>
    </div>
  </div>
</nav>
</template>


<script>
export default {
  name: 'navbar',
  mounted() {
    this.$nextTick(_ => {
      navbar_search_init();
    });
  },
  data () {
    return {
    }
  },
  methods: {
    searchSubmit() {
      console.log('searchSubmit');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>


