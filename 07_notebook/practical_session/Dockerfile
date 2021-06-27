######################################################
# 
# Dockerfile to use RStudio in Docker 
# Based on rocker/rstudio:4.0.2
# bioconductor/bioconductor_docker:RELEASE_3_13
# 
###################################################### 

# Set the base image
FROM bioconductor/bioconductor_docker:RELEASE_3_13

# Install needed R packages
# Don't forget to rebuild the image if this list changes  
RUN install2.r --error --repos http://cran.rstudio.com/ \
    fastqcr \
    shiny

RUN R -e "installed.packages()[,c(3:4)]"