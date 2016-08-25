node {
    echo 'Hello from Pipeline'
    timeout(time:5, unit:'DAYS') {
        input message:'Approve deployment?', submitter: 'it-ops'
    }
    echo "Deploy!"
}
