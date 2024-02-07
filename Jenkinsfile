node {
   checkout scm
   stage("unit-test") {
            echo 'UNIT TEST EXECUTION STARTED'
        }
        stage("functional-test") {
            echo 'FUNCTIONAL TEST EXECUTION STARTED'
        }
        
       stage("synopsys-security-scan") {
              echo 'SYNOPSYS SECURITY SCAN EXECUTION STARTED'
              synopsys_scan product:'blackduck',  blackduck_url: 'https://testing.blackduck.synopsys.com/', blackduck_token: 'NjRhYTY5ZTEtY2M4ZS00YzQ5LTgwZWItMGViNTljYmYxYjc0OjNmZmQ1YzRhLTI3ZGQtNGNmMi05OTM5LWY0MTRjMzdmZjk1Mw==', blackduck_automation_prcomment: true
        }
        
        stage("build") {
              echo 'BUILD EXECUTION STARTED'
              echo 'Pulling...' + env.BRANCH_NAME
       }
       
}
