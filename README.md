# gcloud
configuration

----------------------------------------ubuntu gcloud installation steps------------------------------------------------------- 


https://cloud.google.com/sdk/docs/quickstart-debian-ubuntu


# Create environment variable for correct distribution


CLOUD_SDK_REPO="cloud-sdk-$(grep VERSION_CODENAME /etc/os-release | cut -d '=' -f 2)"

# Add the Cloud SDK distribution URI as a package source


echo "deb http://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

# Import the Google Cloud Platform public key


curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

# Update the package list and install the Cloud SDK


sudo apt-get update && sudo apt-get install google-cloud-sdk


gcloud init


# To continue, you must log in. Would you like to log in (Y/n)? Y

# Pick cloud project to use:
# [1] [my-project-1]
# [2] [my-project-2]
# ...
# Please enter your numeric choice:


gcloud auth list


gcloud config list


gcloud info


