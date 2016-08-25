node {
    stage 'checkout' 
    echo 'Checkout master code'
    stage 'prepare source' 
    echo "Prepare source code"
    stage 'build packages'
    echo "Do something here..."
    stage "Create Artifactory repository"
    echo "Create a repo"
    echo "Copy .deb files to repo"
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
