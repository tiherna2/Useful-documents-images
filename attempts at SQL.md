# Attempts to utilize SQL and RPostgres to create abline/lm

Talia Hernandez

04/01/2022

## Code
      #Begin connection to CENSUS database on postgis.rc.asu.edu
      library(DBI)

      #Make sure to open a connection to sslvpn.asu.edu/2fa through Cisco AnyConnect before running the next command.
      channel <- dbConnect(dr=RPostgres::Postgres(), host = "postgis.rc.asu.edu", dbname="census", user="tiherna2", password="coda")

      #SQL to generate regression variables.

      df <- dbGetQuery(channel, 
                       "SELECT percent_rec_snap, percent_below_poverty,
              FROM acs_2019_snap_w_race

               AND households > 10;")
## Issues

    Error: Failed to prepare query: ERROR:  syntax error at or near "FROM"
    LINE 2:         FROM acs_2019_snap_w_race
                    ^
  
1. I could not find the correct "table" to pull data in from (data base - same issue I encountered before.
2. Then, I utilized "acs_2019_snap_w_race" from the census_build4 table. 
3. Another issue I found was that this build did not have the columns I want to use to answer Q1.
  
## Potential Solutions tried
1. Used package dbplyr to try to translate r into SQL (did not work)
2. Utilized SQL and DBI to connect to database and use acs_2019_snap_w_race as the table to pull columns from. Issue encoded above resulted.
