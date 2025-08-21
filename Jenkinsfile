pipelineJob('job_dsl_plugin') {
  definition {
    cpsScm {
      scm {
        git {
          remote {
            url('https://github.com/todvildes/dsl-jobs.git')
          }
          branch('*/main')
        }
      }
      steps {
        dsl {
          external('jobs/*.groovy')
          removeAction('DISABLE')
          lookupStrategy('SEED_JOB')
          }
        }
      lightweight()
    }
  }
}