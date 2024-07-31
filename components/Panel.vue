<template>
    <v-app>
      <div class="d-flex justify-center text-button darkgrey--text mb-4">ANY QUESTION?</div>
      <div class="d-flex justify-center text-h3 font-weight-bold mb-16">Frequently Asked Questions</div>
      <v-expansion-panels class="mt-4" flat v-model="panel">
        <v-expansion-panel v-for="(item, index) in items" :key="item" class="mb-7" style="max-width: 820px;">
          <v-expansion-panel-header class="text-h6 font-weight-medium">
            {{ item.title }}
            <template v-slot:actions>
              <v-card width="40" height="40" class="d-flex justify-center align-center" rounded="pill" outlined :color="index === panel ? 'rgb(236, 238, 254)' : ''">
                <v-icon :color="index === panel ? 'rgb(81, 103, 246)' : ''">
                  mdi-chevron-down
                </v-icon>
              </v-card>
            </template>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            {{ item.content }}
          </v-expansion-panel-content>
          <v-divider class="mt-5"></v-divider>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-app>
</template>
  
<script>
  export default {
    data() {
      return {
        items: [
          {
            title: "How does JobInn ensure the quality of workers?",
            content: "JobInn workers are rigorously vetted through identity checks and are required to earn certifications from various employers. Additionally, our platform features a robust review and rating system from previous employers and community members, allowing us to maintain and continuously assess the quality of our workforce."
          },
          {
            title: "How does the automated matching system work?",
            content: "Our system uses advanced algorithms to match job postings with qualified workers based on skills, experience, and availability, ensuring a perfect fit for your needs."
          },
          {
            title: "What training and certifications do workers receive?",
            content: "Workers on JobInn can receive training directly from employers who offer their own customized training programs and issue certifications upon completion. Additionally, employers have the ability to review certifications that workers have obtained from previous engagements to determine if they meet their specific job requirements."
          },
          {
            title: "Is there a fee for posting a job or creating an account?",
            content: "Creating an account and posting jobs on JobInn are free. Fees are only incurred when you successfully hire a worker."
          },
          {
            title: "How does JobInn handle compliance and legal requirements?",
            content: "JobInn strictly adheres to local employment laws and regulations, ensuring all hiring practices are compliant and up-to-date."
          },
          {
            title: "What happens if a worker does not meet my expectations?",
            content: "We offer a resolution process to address such issues. Employers can provide feedback and, if necessary, request a different worker to ensure satisfaction."
          }
        ],
      }
    }
  }
</script>