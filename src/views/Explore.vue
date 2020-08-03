<template>
  <div class="container">
    <h1 align="center">Explore Data Projects</h1>
    <b-table striped hover :items="items" :fields="fields" :bordered=true sticky-header> 
      <template v-slot:cell(dataset)="data">
        <!-- `data.value` is the value after formatted by the Formatter -->
        <a :href="`${data.value}`" download>Dataset</a>
      </template>
      <template v-slot:cell(data_analysis)="data">
        <!-- `data.value` is the value after formatted by the Formatter -->
        <a :href="`${data.value}`" download>R Script</a>
      </template>
      <template v-slot:cell(data_visualization)="data">
        <!-- `data.value` is the value after formatted by the Formatter -->
        <a :href="`${data.value}`" target="_blank">Data Visualization</a>
      </template>
    </b-table>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        // Note `isActive` is left out and will not appear in the rendered table
        fields: ['topic', 'dataset', 'data_analysis','data_visualization'],
        items: [
          {
            topic: 'City of Shreveport Budget - 2018',
            dataset: '/analyses/data/01_ExpensesByFundRevenuesByFund.csv',
            data_analysis: '/analyses/expenses.R',
            data_visualization: '/analyses/img/expense.png'
          },
          {
            topic: 'Medicare Psychoses Diagnoses Locations',
            dataset: "/analyses/data/Inpatient_Prospective_Payment_System__IPPS__Provider_Summary_for_the_Top_100_Diagnosis-Related_Groups__DRG__-_FY2011.csv",
            data_analysis: '/analyses/ipps.R',
            data_visualization: '/analyses/img/ipps.png'
          },
          {
            topic: 'NASA Facilities for Entrepreneurs and Innovators Locations',
            dataset: "/analyses/data/NASA_Labs_Facilities.xlsx",
            data_analysis: '/analyses/nasa_locations.R',
            data_visualization: '/analyses/img/nasalocations.png'
          },
          {
            topic: 'World Development Report - 2012',
            dataset: "http://siteresources.worldbank.org/INTWDR2012/Resources/7778105-1299699968583/7786210-1315936222006/Complete-Report.pdf",
            data_analysis: '/analyses/WorldReport2012 - V2.R',
            data_visualization: '/analyses/img/worldreport.png'
          },          
        ],
      }
    },
    methods:{
      
    }
  }
</script>