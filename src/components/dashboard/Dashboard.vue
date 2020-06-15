<template>
  <div class="dashboard">
    <div class="row row-equal">
      <div class="flex xs12 md6 lg6">
        <div class="va-card">
          <div class="va-card__header">
            <div class="va-card__header-inner">Fluentbit Data</div>
          </div>
          <div class="va-card__body va-card__body--padding-top" v-for="content in data" :key="content">
            <p>Version:   {{content.version}}</p>
            <p>Edition:   {{content.edition}}</p>
            <div class="markup-tables">
              <va-card class="mb-2">
                <table class="va-table">
                  <thead>
                    <tr>
                      <th>Flags</th>
                    </tr>
                  </thead>
                  <tr v-for="flag in content.flags" :key="flag">
                    <td>{{ flag}}</td>
                  </tr>
                </table>
              </va-card>
            </div>
          </div>
        </div>
      </div>
    </div>
    <dashboard-charts />
    <dashboard-info-block />
    <div class="row">
      <div class="flex xs12">
        <dashboard-table />
      </div>
    </div>
    <div class="row row-equal">
      <div class="flex xs12 lg6">
        <dashboard-tabs @submit="addAddressToMap"/>
      </div>
      <div class="flex xs12 lg6">
        <dashboard-map ref="dashboardMap"/>
      </div>
    </div>
  </div>
</template>

<script>
import DashboardCharts from './DashboardCharts'
// import DashboardInfoBlock from './DashboardInfoBlock'
// import DashboardTable from './DashboardTable'
// import DashboardTabs from './DashboardTabs'
// import DashboardMap from './DashboardMap'
import axios from 'axios'

export default {
  name: 'dashboard',
  components: {
    DashboardCharts,
    // DashboardInfoBlock,
    // DashboardTable,
    // DashboardTabs,
    // DashboardMap,
  },
  data () {
    return {
      data: [],
    }
  },
  methods: {
    addAddressToMap ({ city, country }) {
      this.$refs.dashboardMap.addAddress({ city: city.text, country })
    },
  },
  mounted () {
    axios
      .get('http://127.0.0.1:2020')
      .then(response => (this.data = response.data))
  },

}
</script>

<style lang="scss">
  .row-equal .flex {
    .va-card {
      height: 100%;
    }
  }

  .dashboard {
    .va-card {
      margin-bottom: 0 !important;
    }
  }
</style>
