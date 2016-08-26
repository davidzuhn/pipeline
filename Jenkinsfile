node {
    stage 'checkout' 
    def buildId = "12345"
    echo "Checkout master code <<< $buildId >>>"
    stage 'prepare source' 
    echo "Prepare source code"
    stage 'build packages'
    echo "Do something here..."
    stage "Create Artifactory repository"
    echo "Create a repo"
    echo "buildId is >>> $buildId <<<"
    echo "Copy .deb files to repo"
    stage 'Build deliverable artifacts'
    parallel 'build-ova':{
      echo "build the OVA"
    }, 'make-updater':{
      echo "create the update bundle"
    }

      
}
node {
    stage 'test'
    echo "test the stuff we just built"
}
