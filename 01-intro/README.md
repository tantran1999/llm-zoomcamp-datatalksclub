## Setup Elastic Search

- Running Elastic Search on local
    ```bash
    docker run -it --rm --name elasticsearch \
        -p 9200:9200 \
        -p 9300:9300 \
        -e "discovery.type=single-node" \
        -e "xpack.security.enabled=false" \
        docker.elastic.co/elasticsearch/elasticsearch:8.4.3
    ```

- Get Elastic Search information
    ```bash
    curl localhost:9200
    ```

- Response
    ```json
    {
        "name" : "c6e52bc57b1e",
        "cluster_name" : "docker-cluster",
        "cluster_uuid" : "rRk39ahUTtiZWb_b1-DXvw",
        "version" : {
            "number" : "8.4.3",
            "build_flavor" : "default",
            "build_type" : "docker",
            "build_hash" : "42f05b9372a9a4a470db3b52817899b99a76ee73",
            "build_date" : "2022-10-04T07:17:24.662462378Z",
            "build_snapshot" : false,
            "lucene_version" : "9.3.0",
            "minimum_wire_compatibility_version" : "7.17.0",
            "minimum_index_compatibility_version" : "7.0.0"
        },
        "tagline" : "You Know, for Search"
    }
    ```