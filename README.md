# lignitetech-web-hugo
LigniteTech web site

## Getting started

Clone the repo  

In the Repo

    git submodule init
    got submodule update

To serve the website locally (linux)

    hugo server -t hugo-universal-theme --bind=0.0.0.0 --baseUrl=http://192.168.0.46 --buildDrafts --buildFuture    

To server the website locally (Windows and Mac)

    hugo server -t hugo-universal-theme --bind=0.0.0.0 --baseUrl=http://localhost --buildDrafts --buildFuture
