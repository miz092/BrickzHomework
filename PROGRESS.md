### PROGRESS REPORT

#### Installing prerequisites

    - I chose to install Superset using docker compose - since I have Windows OS - which was a simple and straightforward process with the help of 
    the official documentation. 

Link: [Official documentation on installation](https://superset.apache.org/docs/installation/installing-superset-using-docker-compose)


### Task 1 

    - Ábrázold egy kördiagrammon, hogy a userek hány szöveggel rendelkező
    message-t írtak channel-enként. A lekérdezést mentsd el egy chart-ba, azt pedig
    egy dashboard-ba. A dashboard-ban lehessen szűrni tetszőleges mennyiségű
    channel-re és user-re, továbbá a message küldésének időpontjára(intervallum, pl.
    csak a 2019-es message-k).


#### Chart creation
At first I thought the easiest way is to write a query in SQL LAB so I did just that:
```sql
SELECT channel_id, COUNT(channel_id) as message_count from messages
where client_msg_id IS NOT NULL
group by channel_id
order by message_count desc
```

This worked like a charm, - however I started to grasp what Superset is really about. It turned out I didn't need to write any queries to finish 
this task, as the program itself has functionality for simple aggregations like this. 

I started to create a new chart on the messages table: 
    - for dimensions I chose channel_id
    - I created a new metric called 'Message count'
    - also added a filter to exclude 'client_msg_id'-s with NULL values
    
#### Dashboard creation

Creating the dashboard was fairly a straightforward process, the UI provides a clean and easily understandable platform to create filters.
However, I was a little confused at first about the date picking part, so I created an extra field in the table where I extracted the year from the 
timestamp, so I could filter them by year - as the task description suggested it - but then I found the appropriate tool among the filter options. 


### Task 2

#### Chart creation

#### Dashboard creation

### Completion Time Overview