# RxNav-in-a-Box

[Download Link](https://download.nlm.nih.gov/umls/kss/rxnav/rxnav-in-a-box/rxnav-in-a-box-20251201.zip)

RxNav-in-a-Box provides RxNav APIs and applications as Open
Container Initiative ("Docker") containers, coordinated by Docker
Compose, so they can be deployed on any machine without needing to
rely on the NLM webserver.

RxNav-in-a-Box is designed for individual, personal use.

RxNav-in-a-Box includes the following APIs and applications:

APIs
  RxNorm API               see <https://rxnav.nlm.nih.gov/RxNormAPIs.html>
  RxClass API              see <https://rxnav.nlm.nih.gov/RxClassAPIs.html>
  Prescribable RxNorm API  see <https://rxnav.nlm.nih.gov/PrescribableAPIs.html>
  RxTerms API              see <https://rxnav.nlm.nih.gov/RxTermsAPIs.html>

Apps
  RxNav                    see <https://rxnav.nlm.nih.gov/RxNavDoc.html>
  RxClass                  see <https://rxnav.nlm.nih.gov/RxClassIntro.html>
  RxMix                    see <https://rxnav.nlm.nih.gov/RxMixTutorial.html>

The API functions getApproximateMatch and getProprietaryInformation in
RxNav-in-a-Box do not accept a UTS API key.

To access RxNorm data directly with SQL queries, please download and
use the RxNorm full release and Technical Documentation from
<https://www.nlm.nih.gov/research/umls/rxnorm/docs/rxnormfiles.html> .

## SYSTEM REQUIREMENTS

- 12 gigabytes of memory to devote to a container platform (e.g., Docker)

- 100 gigabytes of disk space

- Docker Desktop,
   or another OCI-compatible platform (in which case you
   may take the included docker-compose.yml file as an example).

## INSTALLATION

 1. Make sure Docker Desktop is installed and running on your computer.

 2. If your computer runs Windows, put Docker Desktop into the mode to
    run Linux containers.

 3. If your system limits the memory, swap space, or disk
    space that containers may use in the aggregate, raise the limits to
    12GB memory, 4GB swap, and 100GB disk space.

 4. Unzip the RxNav-in-a-Box zip file.

    The resulting files look like this:

        rxnav-in-a-box-20191007/
            README.txt
            docker-compose.yml
            ...
          
 5. Start the Docker containers from docker-compose.yml:  Using Docker
    Compose on your computer's command line, you may try

        cd rxnav-in-a-box-20191007
        docker-compose up

    The "docker-compose up" may take about an hour to import
    the included RxNav data.

    - Docker Desktop might pop-up to ask about "file sharing".  It
      needs access to the place where you unzipped RxNav-in-a-Box.

    - If Docker says "ERROR: no matching manifest for windows/amd64...",
      your Docker Desktop might be running in Windows container mode.
      You will need to switch it to Linux containers.

    - If Docker says "disk full", it might be referring
      to a reserved, limited space for Docker images on your computer.  
      You might be able to enlarge that space.

    - Avoid interrupting the containers until the "docker-compose up"
      console messages show "MariaDB init process done. Ready for
      start up" or messages from the rxapis container cease repeating
      "Periodically checking rxnav-db" and move on to further
      progress.  If there is an interruption before that point, the
      database might be incomplete.  Remove the partially-initialized
      RxNav-in-a-Box containers, clear Docker's caches, and try
      "docker-compose up" again.

 6. You may adjust your computer's firewall to control whether or not
    other machines on your network might be able to use your
    RxNav-in-a-Box.  The relevant port is TCP port 4000.

 7. RxNav-in-a-Box is now ready to use.

    Please refer to the docker-compose documentation for guidance
    on stopping and restarting containers so as not to repeat the
    lengthy setup.

## HOW TO USE

 1. In a terminal:

        cd rxnav-in-a-box-20191007
        docker-compose up

 2. Point your web browser to <http://localhost:4000/>
