# Dreamforce 23 - Adopt Package Based Development with Org-Dependent Packaging

Repository for the org-dependent package demonstrated in my Dreamforce 23 theatre session.
The package contains references to metadata that doesn't exist in this repository, but it package versions can still be created. 

## Installation

### Pre-requisites

Install the metadata from the "Happy Soup" repository for this session, which you can find at [https://github.com/keirbowden/DF23HappySoup](https://github.com/keirbowden/DF23HappySoup)

### Instructions

This package must be installed using the Salesforce CLI. Execute the following command to install it:

`sf package install -w 30 -p 04t4L00000051JHQAY {-o <username>}`

where `<username>` is the username for the org you want to install the package into, that you have previously authenticated using the CLI.

## Setup

Assign the Bookstore with Readings permission set group to your user.

`sf org assign permset -n 'Bookstore_with_Readings' {-o <username>}`

Create the sample data using the following command:

`sf apex run -f ./scripts/apex/setup_data.apex {-o <username>}`

## Accessing

Open the org.
Access the `Bookstore with Readings` application 
Open the BookSearch page and marvel at the new Reading Results.
