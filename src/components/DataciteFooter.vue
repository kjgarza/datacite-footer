<template>

<div class='row footer'>
  <!-- <div class="container-fluid"> -->
    <div class='col-md-3'>
      <h4>About DataCite</h4>
      <ul>
        <li v-for="link in aboutLinks" :key="link.id">
          <a v-bind:href="link.url">{{ link.name  }}</a>
        </li>
      </ul>
    </div>
    <div class='col-md-3'>
      <h4>Services</h4>
      <ul>
        <li v-for="link in servicesLinks" :key="link.id">
          <a v-bind:href="link.url">{{ link.name  }}</a>
        </li>
      </ul>
    </div>
    <div class='col-md-3'>
      <h4>Resources</h4>
      <ul>
        <li v-for="link in resourcesLinks" :key="link.id">
          <a v-bind:href="link.url">{{ link.name  }}</a>
        </li>
      </ul>
      <h4>Community</h4>
      <ul>
        <li v-for="link in communityLinks" :key="link.id">
          <a v-bind:href="link.url">{{ link.name  }}</a>
        </li>
      </ul>
    </div>
    <div class='col-md-3'>
      <h4 class="share">Contact us</h4>
      <a href='mailto:support@datacite.org' class="share">
        <i class='fa fa-at'></i>
      </a>
      <a href='https://blog.datacite.org/feed.xml' class="share">
        <i class='fa fa-rss'></i>
      </a>
      <a href='https://twitter.com/datacite' class="share">
        <i class='fa fa-twitter'></i>
      </a>
      <a href='https://github.com/datacite/datacite' class="share">
        <i class='fa fa-github'></i>
      </a>
      <a href='https://www.linkedin.com/company/datacite' class="share">
        <i class='fa fa-linkedin'></i>
      </a>
      <ul>
        <li v-for="link in contactLinks" :key="link.id">
          <a v-bind:href="link.url">{{ link.name  }}</a>
        </li>
      </ul>
      <a href="http://status.datacite.org" target="_blank">
        <span class="color-dot"></span>
        <span class="color-description"></span>
      </a>
    </div>
  <!-- </div> -->
</div>
</template>

<script>
export default {
  name: 'DataciteFooter',
  props: {
    title: String
  },
  data: function() { 
    return {
      aboutLinks: [
    {
      "name": "What we do",
      "url": "https://www.datacite.org/mission.html"
    },
    {
      "name": "Governance",
      "url": "https://www.datacite.org/governance.html"
    },
    {
      "name": "Steering groups",
      "url": "https://www.datacite.org/steering.html"
    },
    {
      "name": "Staff",
      "url": "https://www.datacite.org/staff.html"
    },
    {
      "name": "Job opportunities",
      "url": "https://www.datacite.org/jobopportunities.html"
    }
  ],
      servicesLinks: [
    {
      "name": "Assign DOIs",
      "url": "https://www.datacite.org/dois.html"
    },
    {
      "name": "Metadata search",
      "url": "https://www.datacite.org/search.html"
    },
    {
      "name": "Event data",
      "url": "https://www.datacite.org/eventdata.html"
    },
    {
      "name": "Profiles",
      "url": "https://www.datacite.org/profiles.html"
    },
    {
      "name": "re3data",
      "url": "https://www.datacite.org/re3data.html"
    },
    {
      "name": "Citation formatter",
      "url": "https://www.datacite.org/citation.html"
    },
    {
      "name": "Statistics",
      "url": "https://www.datacite.org/stats.html"
    },
    {
      "name": "Content negotiation",
      "url": "https://www.datacite.org/content.html"
    },
    {
      "name": "OAI-PMH",
      "url": "https://www.datacite.org/oaipmh.html"
    }
  ],
      resourcesLinks: [
    {
      "name": "Metadata schema",
      "url": "https://schema.datacite.org"
    },
    {
      "name": "Support",
      "url": "https://support.datacite.org"
    }
  ],
      communityLinks: [
    {
      "name": "Members",
      "url": "https://www.datacite.org/members.html"
    },
    {
      "name": "Partners",
      "url": "https://www.datacite.org/partners.html"
    },
    {
      "name": "Steering groups",
      "url": "https://www.datacite.org/steering.html"
    },
    {
      "name": "Events",
      "url": "https://www.datacite.org/events.html"
    },
    {
      "name": "Roadmap",
      "url": "https://www.datacite.org/roadmap.html"
    },
    {
      "name": "User Stories",
      "url": "https://www.datacite.org/user-stories.html"
    }
  ],
      contactLinks: [
    {
      "name": "Terms and conditions",
      "url": "https://www.datacite.org/terms.html"
    },
    {
      "name": "Privacy policy",
      "url": "https://www.datacite.org/privacy.html"
    },
    {
      "name": "Acknowledgements",
      "url": "https://www.datacite.org/acknowledgments.html"
    }
  ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

@import url('https://fonts.googleapis.com/css?family=Raleway:400,600,400italic,600italic');


div.footer {
  position: absolute;
  bottom: 0;
  height: 300px;
  width: 100%;
  color: #9A9AA8;
  font-weight: 300;
  background-color: #E3E3E3;
  padding: .75em 0;
  margin: 0;
  }
  h4, h5 {
    font-size: 15;
    font-weight: 600;
    margin-top: .5em;
    margin-bottom: .1em;
    line-height: 1.2em;
    -webkit-font-smoothing: antialiased;
    font-family: "Raleway", "Helvetica", Arial, sans-serif;
  }
  ul {
    list-style: none;
    padding-left: 0;
  }
  a, a:hover, a:visited {
    color: #9A9AA8;
  }
  .share h4 {
    color: gray;
    margin-bottom: .5em;
  }
  .share a {
    margin-right: 1em;
    font-size: 16px;
  }
</style>
