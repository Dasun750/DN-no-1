<template>
  <q-layout view="hHh Lpr lff">
    <q-header elevated class="bg-deep-purple-7 text-white">
      <q-toolbar class="q-py-md">
        <q-toolbar-title class="row items-center no-wrap">
          <q-avatar>
            <img src="https://source.unsplash.com/random/100x100/?cricket,ball,colorful" />
          </q-avatar>
          <span class="q-ml-md text-h5">Global Cricket Hub</span>
        </q-toolbar-title>

        <q-space />

        <q-tabs v-model="tab" align="left" class="q-mx-md" active-color="yellow" indicator-color="yellow">
          <q-tab name="home" label="Home" />
          <q-tab name="news" label="News" />
          <q-tab name="fixtures" label="Fixtures" />
          <q-tab name="teams" label="Teams" />
          <q-tab name="stats" label="Stats" />
        </q-tabs>

        <q-space />

        <div class="q-gutter-sm">
          <q-btn flat round icon="search" />
          <q-btn flat round icon="person" />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <q-page class="q-pa-md">
        <!-- Hero Section -->
        <div class="hero-section relative-position" style="height: 500px; border-radius: 12px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.2);">
          <img src="https://source.unsplash.com/random/1600x900/?cricket,stadium,colorful" style="width: 100%; height: 100%; object-fit: cover;" />
          <div class="absolute-full flex flex-center" style="background: linear-gradient(135deg, rgba(101,31,255,0.6) 0%, rgba(255,31,171,0.6) 100%);">
            <div class="text-center">
              <div class="text-h2 text-weight-bold" style="text-shadow: 2px 2px 4px rgba(0,0,0,0.5);">Global Cricket Hub</div>
              <div class="text-h5 q-mt-sm" style="text-shadow: 1px 1px 3px rgba(0,0,0,0.5);">Your ultimate destination for cricket news, stats, and updates</div>
              <q-btn color="yellow" text-color="deep-purple-9" class="q-mt-xl q-px-xl q-py-sm" size="large" label="Explore Now" />
            </div>
          </div>
        </div>

        <!-- Latest News Section -->
        <div class="q-mt-xl">
          <div class="text-h4 q-mb-md text-deep-purple-8">Latest News</div>
          <q-separator color="deep-purple-4" />

          <div class="row q-col-gutter-md q-mt-md">
            <div class="col-12 col-md-4" v-for="n in 3" :key="n">
              <q-card class="news-card">
                <q-img src="https://source.unsplash.com/random/600x400/?cricket,match,colorful"
                       height="200px"
                       :ratio="16/9" />

                <q-card-section class="bg-deep-purple-1">
                  <div class="text-subtitle2 text-deep-purple-8">Match Report</div>
                  <div class="text-h6">England clinches thrilling victory against Australia in the final over</div>
                </q-card-section>

                <q-card-section class="q-pt-none bg-deep-purple-1">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </q-card-section>

                <q-card-actions align="right" class="bg-deep-purple-1">
                  <q-btn flat color="deep-purple-8" label="Read More" />
                </q-card-actions>
              </q-card>
            </div>
          </div>
        </div>

        <!-- Upcoming Matches -->
        <div class="q-mt-xl">
          <div class="text-h4 q-mb-md text-deep-purple-8">Upcoming Matches</div>
          <q-separator color="deep-purple-4" />

          <div class="row q-col-gutter-md q-mt-md">
            <div class="col-12 col-md-6 col-lg-3" v-for="n in 4" :key="n">
              <q-card class="match-card">
                <q-card-section class="bg-gradient" style="background: linear-gradient(135deg, #651fff 0%, #ff1fa0 100%);">
                  <div class="row items-center no-wrap">
                    <div class="col-4 flex flex-center">
                      <q-avatar size="60px" class="q-shadow-3">
                        <img src="https://source.unsplash.com/random/100x100/?cricket,flag,colorful" />
                      </q-avatar>
                    </div>
                    <div class="col-4 flex flex-center">
                      <div class="text-h6 text-white" style="text-shadow: 1px 1px 2px rgba(0,0,0,0.5);">VS</div>
                    </div>
                    <div class="col-4 flex flex-center">
                      <q-avatar size="60px" class="q-shadow-3">
                        <img src="https://source.unsplash.com/random/100x100/?cricket,flag,colorful" />
                      </q-avatar>
                    </div>
                  </div>
                </q-card-section>

                <q-card-section class="bg-white">
                  <div class="text-subtitle2 text-deep-purple-6">T20 World Cup 2025</div>
                  <div class="text-h6 text-deep-purple-9">India vs Pakistan</div>
                  <div class="text-subtitle2 text-grey-8">MCG, Melbourne</div>
                </q-card-section>

                <q-card-section class="q-pt-none bg-white">
                  <q-icon name="schedule" color="deep-purple-6" /> <span class="text-grey-8">15 Feb 2025, 19:00 Local</span>
                </q-card-section>

                <q-card-actions align="right" class="bg-white">
                  <q-btn flat color="deep-purple-8" label="Match Details" />
                </q-card-actions>
              </q-card>
            </div>
          </div>
        </div>

        <!-- Featured Player -->
        <div class="q-mt-xl">
          <div class="text-h4 q-mb-md text-deep-purple-8">Featured Player</div>
          <q-separator color="deep-purple-4" />

          <q-card class="q-mt-md featured-player">
            <div class="row">
              <div class="col-12 col-md-4">
                <q-img src="https://source.unsplash.com/random/600x800/?cricket,player,portrait"
                       :ratio="3/4"
                       style="height: 100%"
                       position="center" />
              </div>
              <div class="col-12 col-md-8 q-pa-md bg-deep-purple-1">
                <div class="text-h4 text-deep-purple-9">Kane Williamson</div>
                <div class="text-subtitle1 text-deep-purple-6">New Zealand</div>

                <q-separator class="q-my-md" color="deep-purple-3" />

                <div class="row q-col-gutter-md">
                  <div class="col-6 col-md-3">
                    <q-card class="stat-card bg-deep-purple-2 q-pa-sm">
                      <div class="text-subtitle2 text-deep-purple-6">Test Matches</div>
                      <div class="text-h5 text-deep-purple-9">89</div>
                    </q-card>
                  </div>
                  <div class="col-6 col-md-3">
                    <q-card class="stat-card bg-deep-purple-2 q-pa-sm">
                      <div class="text-subtitle2 text-deep-purple-6">ODIs</div>
                      <div class="text-h5 text-deep-purple-9">157</div>
                    </q-card>
                  </div>
                  <div class="col-6 col-md-3">
                    <q-card class="stat-card bg-deep-purple-2 q-pa-sm">
                      <div class="text-subtitle2 text-deep-purple-6">T20Is</div>
                      <div class="text-h5 text-deep-purple-9">87</div>
                    </q-card>
                  </div>
                  <div class="col-6 col-md-3">
                    <q-card class="stat-card bg-deep-purple-2 q-pa-sm">
                      <div class="text-subtitle2 text-deep-purple-6">Career Avg</div>
                      <div class="text-h5 text-deep-purple-9">52.68</div>
                    </q-card>
                  </div>
                </div>

                <q-separator class="q-my-md" color="deep-purple-3" />

                <div class="text-body1 text-grey-8">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam quam neque, efficitur eu consequat vitae, vestibulum at nibh. Praesent euismod, tortor in efficitur feugiat, nulla nisi ultrices nulla, vel finibus urna mauris et dolor.
                </div>

                <q-btn color="deep-purple-7" label="Full Profile" class="q-mt-md q-px-md" />
              </div>
            </div>
          </q-card>
        </div>

        <!-- Video Highlights -->
        <div class="q-mt-xl">
          <div class="text-h4 q-mb-md text-deep-purple-8">Video Highlights</div>
          <q-separator color="deep-purple-4" />

          <div class="row q-col-gutter-md q-mt-md">
            <div class="col-12 col-md-6" v-for="n in 2" :key="n">
              <q-card class="video-card">
                <q-responsive :ratio="16/9">
                  <div class="bg-grey-2 absolute-full flex flex-center">
                    <q-icon name="play_circle_filled" size="5rem" class="text-white q-shadow-5" style="z-index: 1;" />
                    <img src="https://source.unsplash.com/random/800x450/?cricket,celebration,colorful" style="width: 100%; height: 100%; object-fit: cover;" />
                  </div>
                </q-responsive>

                <q-card-section class="bg-deep-purple-1">
                  <div class="text-h6 text-deep-purple-8">Tournament Highlights: Best moments from the Asia Cup 2025</div>
                </q-card-section>

                <q-card-section class="q-pt-none bg-deep-purple-1">
                  <q-icon name="schedule" color="deep-purple-6" /> <span class="text-grey-7">Posted 2 days ago</span>
                </q-card-section>
              </q-card>
            </div>
          </div>
        </div>
      </q-page>
    </q-page-container>

    <q-footer elevated class="bg-deep-purple-9 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <div>Global Cricket Hub &copy; 2025</div>
        </q-toolbar-title>

        <div>
          <q-btn flat round icon="facebook" />
          <q-btn flat round icon="twitter" />
          <q-btn flat round icon="instagram" />
          <q-btn flat round icon="youtube" />
        </div>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {
      tab: 'home'
    }
  }
}
</script>

<style lang="scss">
.news-card, .match-card, .video-card, .featured-player, .stat-card {
  transition: all 0.3s ease;
  border-radius: 12px;
  overflow: hidden;

  &:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(101, 31, 255, 0.15);
  }
}

.hero-section {
  box-shadow: 0 15px 30px rgba(101, 31, 255, 0.2);
}

.stat-card {
  border-radius: 8px;
  transition: all 0.2s ease;

  &:hover {
    background: #d1c4e9 !important;
    transform: scale(1.05);
  }
}
</style>
