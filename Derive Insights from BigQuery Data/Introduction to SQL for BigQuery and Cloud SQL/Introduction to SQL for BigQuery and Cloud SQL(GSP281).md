# Introduction to SQL for BigQuery and Cloud SQL || [GSP281](https://www.cloudskillsboost.google/course_templates/623/labs/489280) ||

### Run the following Commands in CloudShell

### From "Task 5. Create a Cloud SQL instance" you can find your REGION,

```
export REGION=
```
```

BLACK=`tput setaf 0`
RED=`tput setaf 1`
GREEN=`tput setaf 2`
YELLOW=`tput setaf 3`
BLUE=`tput setaf 4`
MAGENTA=`tput setaf 5`
CYAN=`tput setaf 6`
WHITE=`tput setaf 7`

BG_BLACK=`tput setab 0`
BG_RED=`tput setab 1`
BG_GREEN=`tput setab 2`
BG_YELLOW=`tput setab 3`
BG_BLUE=`tput setab 4`
BG_MAGENTA=`tput setab 5`
BG_CYAN=`tput setab 6`
BG_WHITE=`tput setab 7`

BOLD=`tput bold`
RESET=`tput sgr0`
#----------------------------------------------------start--------------------------------------------------#

echo "${YELLOW}${BOLD}Starting${RESET}" "${GREEN}${BOLD}Execution${RESET}"

gsutil mb gs://$DEVSHELL_PROJECT_ID

curl -O https://raw.githubusercontent.com/Himadri8991/Google-Arcade-Skill-Badges-Solutions/main/Derive%20Insights%20from%20BigQuery%20Data/Introduction%20to%20SQL%20for%20BigQuery%20and%20Cloud%20SQL/start_station_name.csv

curl -O https://raw.githubusercontent.com/Himadri8991/Google-Arcade-Skill-Badges-Solutions/main/Derive%20Insights%20from%20BigQuery%20Data/Introduction%20to%20SQL%20for%20BigQuery%20and%20Cloud%20SQL/end_station_name.csv

gsutil cp start_station_name.csv gs://$DEVSHELL_PROJECT_ID/
gsutil cp end_station_name.csv gs://$DEVSHELL_PROJECT_ID/

gcloud sql instances create my-demo \
    --database-version=MYSQL_5_7 \
    --region=$REGION \
    --tier=db-f1-micro \
    --root-password=quicklab

gcloud sql databases create bike --instance=my-demo

echo "${RED}${BOLD}Congratulations${RESET}" "${WHITE}${BOLD}for${RESET}" "${GREEN}${BOLD}Completing the Lab !!!${RESET}"
echo "${RED}${BOLD}With Regards Himadri${RESET}"

#-----------------------------------------------------end----------------------------------------------------------#

```


### Congratulations 🎉 for completing the Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/Cxmw4DvCwEHCqU8qzTpv6r) 
