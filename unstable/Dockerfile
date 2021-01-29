#
# SPDX-License-Identifier: Apache-2.0
#
FROM ibmcom/ibp-microfab

USER root
COPY fabric/release/linux-amd64/ /opt/fabric/
RUN mkdir -p /var/hyperledger && chown 7051:7051 /var/hyperledger

USER 7051
