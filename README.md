# transitgatway-infra-app
# AWS Transit Gateway Sharing Infrastructure
    This repository contains the Infrastructure as Code (IaC) necessary to set up an AWS Transit Gateway (TGW) and share it across multiple AWS accounts to enable efficient and centralized traffic routing. The setup leverages AWS services such as VPCs, Transit Gateway, Resource Access Manager (RAM), and appropriate IAM permissions to facilitate routing across multiple accounts within an AWS Organization.


# Overview
    The project enables efficient inter-VPC routing across multiple AWS accounts using a centrally managed Transit Gateway (TGW). By sharing the TGW, you can reduce network complexity and manage routing in one place while enabling communication between VPCs in different accounts without requiring VPC peering.

    Transit Gateway provides a hub-and-spoke model to route traffic between multiple VPCs and on-premises networks.
    Resource Access Manager (RAM) is used to share the TGW with other AWS accounts.
    AWS Organization is leveraged for managing multiple AWS accounts.

# Architecture
    The architecture is composed of:
        Central Account: Hosts the Transit Gateway and shares it with participant accounts.
        Participant Accounts: Accounts where VPCs are attached to the shared Transit Gateway for inter-VPC communication.
        Transit Gateway: Deployed in the central account.
        VPC Attachments: VPCs in different participant accounts attach to the Transit Gateway.
        RAM Sharing: Transit Gateway is shared with participant accounts via AWS RAM.

