# Please choose from the below set of Docker commands to complete your Dockerfile:

# COPY
# RUN
# ADD
# EXPOSE
# FROM
# CMD
# PUSH
# PULL
# WORKDIR


FROM golang:1.18 AS builder

WORKDIR /app

COPY main.go .

RUN go mod init guestbook
RUN go mod tidy

RUN go build -o main main.go

FROM ubuntu:18.04

COPY --from=builder /app/main /app/guestbook

COPY public/index.html /app/public/index.html
COPY public/script.js /app/public/script.js
COPY public/style.css /app/public/style.css
COPY public/jquery.min.js /app/public/jquery.min.js

WORKDIR /app

CMD ["./guestbook"]
EXPOSE 3000



#theia@theiaopenshift-zachary007:/home/project/guestbook/v1$ export MY_NAMESPACE=sn-labs-$USERNAME
# theia@theiaopenshift-zachary007:/home/project/guestbook/v1/guestbook$ docker build . -t us.icr.io/$MY_NAMESPACE/guestbook:v1
# [+] Building 97.4s (19/19) FINISHED
# theia@theiaopenshift-zachary007:/home/project/guestbook/v1/guestbook$ docker push us.icr.io/$MY_NAMESPACE/guestbook:v1
# The push refers to repository [us.icr.io/sn-labs-zachary007/guestbook]
# 5f70bf18a086: Pushed 
# cf84d7c4e778: Pushed 
# 48417fb43e89: Pushed 
# 236a0eafd7b4: Pushed 
# dd1d8fe2cdf8: Pushed 
# 25529f49a5e3: Pushed 
# 548a79621a42: Pushed 
# v1: digest: sha256:c3c24a10a9eb664ed281c9f43944979c1e11c200bba96855990228819ffb8f41 size: 1776
# theia@theiaopenshift-zachary007:/home/project/guestbook/v1/guestbook$ ibmcloud cr images
# Listing images...

# Repository                                                               Tag                                                                           Digest         Namespace            Created         Size     Security status
# us.icr.io/sn-labs-zachary007/guestbook                                   v1                                                                            c3c24a10a9eb   sn-labs-zachary007   3 minutes ago   32 MB    -
# us.icr.io/sn-labsassets/categories-watson-nlp-runtime                    latest                                                                        6b01b1e5527b   sn-labsassets        3 years ago     3.1 GB   -
# us.icr.io/sn-labsassets/classification-watson-nlp-runtime                latest                                                                        dbd407898549   sn-labsassets        3 years ago     4.0 GB   -
# us.icr.io/sn-labsassets/concepts-watson-nlp-runtime                      latest                                                                        1e4741f10569   sn-labsassets        3 years ago     3.2 GB   -
# us.icr.io/sn-labsassets/custom-watson-nlp-runtime                        latest                                                                        f6513e19a33d   sn-labsassets        3 years ago     6.5 GB   -
# us.icr.io/sn-labsassets/detag-watson-nlp-runtime                         latest                                                                        38916c2119fc   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/emotion-watson-nlp-runtime                       latest                                                                        1c9de1d27318   sn-labsassets        3 years ago     4.0 GB   -
# us.icr.io/sn-labsassets/entity-mentions-bert-watson-nlp-runtime          latest                                                                        57d92957214f   sn-labsassets        3 years ago     3.8 GB   -
# us.icr.io/sn-labsassets/entity-mentions-bilstm-watson-nlp-runtime        latest                                                                        76dbd3bdb12b   sn-labsassets        3 years ago     2.9 GB   -
# us.icr.io/sn-labsassets/entity-mentions-rbr-multi-watson-nlp-runtime     latest                                                                        577399d7b4e7   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/entity-mentions-rbr-watson-nlp-runtime           latest                                                                        506cc92ecd3f   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/entity-mentions-sire-watson-nlp-runtime          latest                                                                        cd4e48efd3f6   sn-labsassets        3 years ago     2.8 GB   -
# us.icr.io/sn-labsassets/entity-mentions-transformer-watson-nlp-runtime   latest                                                                        0584c56563ce   sn-labsassets        3 years ago     3.8 GB   -
# us.icr.io/sn-labsassets/instructions-splitter                            latest                                                                        2af122cfe4ee   sn-labsassets        5 years ago     21 MB    -
# us.icr.io/sn-labsassets/istio-examples-bookinfo-details-v1               1.17.0                                                                        85819dbebb6d   sn-labsassets        4 years ago     62 MB    -
# us.icr.io/sn-labsassets/istio-examples-bookinfo-productpage-v1           1.17.0                                                                        4c58e1fbe731   sn-labsassets        4 years ago     68 MB    -
# us.icr.io/sn-labsassets/istio-examples-bookinfo-ratings-v1               1.17.0                                                                        f529526d2807   sn-labsassets        4 years ago     57 MB    -
# us.icr.io/sn-labsassets/istio-examples-bookinfo-reviews-v3               1.17.0                                                                        0b37c5a396f7   sn-labsassets        4 years ago     415 MB   -
# us.icr.io/sn-labsassets/keywords-watson-nlp-runtime                      latest                                                                        e2b9dc471ae0   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/lang-detect-watson-nlp-runtime                   latest                                                                        4d3b44e72af0   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/llmchatbot-demo                                  latest                                                                        b0c45851acbe   sn-labsassets        3 years ago     5.1 GB   -
# us.icr.io/sn-labsassets/nginx                                            1.25.1                                                                        73e957703f12   sn-labsassets        3 years ago     71 MB    -
# us.icr.io/sn-labsassets/nginx                                            latest                                                                        73e957703f12   sn-labsassets        3 years ago     71 MB    -
# us.icr.io/sn-labsassets/nginx                                            sha256-85eabf2757cb5b5b84248d7feb019079501dfd8691fc79b8b1d0ff1591a6270b.sig   9a38ca67e16d   sn-labsassets        -               308 B    -
# us.icr.io/sn-labsassets/nginx                                            signed                                                                        85eabf2757cb   sn-labsassets        3 years ago     67 MB    -
# us.icr.io/sn-labsassets/nginx                                            unsigned                                                                      73e957703f12   sn-labsassets        3 years ago     71 MB    -
# us.icr.io/sn-labsassets/noun-phrases-watson-nlp-runtime                  latest                                                                        c696f6af9797   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/openshift-console-auth-proxy                     0.0.1                                                                         f3cd15bd3584   sn-labsassets        6 years ago     355 MB   -
# us.icr.io/sn-labsassets/pgadmin-theia                                    latest                                                                        0adf67ad81a3   sn-labsassets        5 years ago     101 MB   -
# us.icr.io/sn-labsassets/phpmyadmin                                       latest                                                                        b66c30786353   sn-labsassets        5 years ago     163 MB   -
# us.icr.io/sn-labsassets/relations-sire-watson-nlp-runtime                latest                                                                        65c2e74995d5   sn-labsassets        3 years ago     2.8 GB   -
# us.icr.io/sn-labsassets/relations-transformer-watson-nlp-runtime         latest                                                                        18ffd6c35726   sn-labsassets        3 years ago     3.6 GB   -
# us.icr.io/sn-labsassets/relations-watson-nlp-runtime                     latest                                                                        3547dcc15c43   sn-labsassets        3 years ago     3.6 GB   -
# us.icr.io/sn-labsassets/sentiment-bert-watson-nlp-runtime                latest                                                                        b7f6814ca014   sn-labsassets        3 years ago     3.7 GB   -
# us.icr.io/sn-labsassets/sentiment-cnn-watson-nlp-runtime                 latest                                                                        d89e9fbfccf1   sn-labsassets        3 years ago     2.8 GB   -
# us.icr.io/sn-labsassets/sentiment-watson-nlp-runtime                     latest                                                                        a0b76bd2dad7   sn-labsassets        3 years ago     4.2 GB   -
# us.icr.io/sn-labsassets/speech-standalone                                latest                                                                        635f94bc2c1c   sn-labsassets        3 years ago     3.7 GB   -
# us.icr.io/sn-labsassets/syntax-watson-nlp-runtime                        latest                                                                        332c147eb437   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/tts-standalone                                   latest                                                                        56ce85280714   sn-labsassets        3 years ago     3.7 GB   -
# us.icr.io/sn-labsassets/tts-standalone-full                              latest                                                                        0285cd4b20bd   sn-labsassets        3 years ago     5.4 GB   -
# us.icr.io/sn-labsassets/watson-nlp-runtime                               1.0.18                                                                        0cbcbd5bde0e   sn-labsassets        3 years ago     2.7 GB   -
# us.icr.io/sn-labsassets/watson-nlp_syntax_izumo_lang_en_stock            1.0.7                                                                         362ba4b6ef00   sn-labsassets        3 years ago     14 MB    -
# us.icr.io/sn-labsassets/watson-nlp_syntax_izumo_lang_fr_stock            1.0.7                                                                         2d47c44882c7   sn-labsassets        3 years ago     14 MB    -

# OK
# theia@theiaopenshift-zachary007:/home/project/guestb
# theia@theiaopenshift-zachary007:/home/project/guestbook/v1/guestbook$ 