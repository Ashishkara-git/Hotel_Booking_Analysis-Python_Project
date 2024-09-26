# Hotel_Booking_Analysis-Python_project

## Project Overview

This project analyzes high cancellation rates at City Hotel and Resort Hotel, exploring their impact on revenue and occupancy. It aims to identify the causes of cancellations and provide actionable recommendations to reduce them, ultimately enhancing operational efficiency and boosting revenue for both hotels.

## Research Question

1. What are the variables that affect hotel reservation cancellation?
2. How can we make hotel reservation cancellations better?
3. How will hotels be assisted in making pricing and promotional decisions? 


## Data Sources

Hotel Booking Data: The primary dataset used for this analysis is the [hotel_booking.csv](https://www.kaggle.com/datasets/mojtaba142/hotel-booking/data) file, containing detailed information about hotel bookings.  

## Tools

Python and its libraries
- numpy
- pandas 
- matplotlib
- seaborn

## Data Cleaning/Preparation

In the initial data preparation Phase, we performed the following taskes:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleasing and formatting. 

## Data Analysis

Include some inetresting code/feature worked with

```sns.set_style('darkgrid')
a=sns.countplot(x=df.is_canceled,palette='Blues',edgecolor='k')
plt.title('Reservation status count',size=18)
plt.xticks([0,1],['Not Canceled','Canceled'])
for i in a.containers:
    a.bar_label(i)
plt.show()
```

```plt.figure(figsize=(20,7))
canceled_adr = canceled_data.groupby('reservation_status_date')[['adr']].mean()
canceled_adr.reset_index(inplace=True)

not_canceled_data = df[df['is_canceled']==0]
not_canceled_adr = not_canceled_data.groupby('reservation_status_date')[['adr']].mean().reset_index()
```

## Sample Visuals

![alt text](image.png)

![alt text](image-1.png)


## Suggestions

1. Cancellation rates rise as the price does. In order to prevent cancellation of reservations, hotels could work on their pricing strategies and try to lower the rates for specific hotels based on locations. They can also provide some discounts to consumers.

2. As the ration of the cancellation and not cancellation of the resort hotels is higher in than city hotels. So, the hotels should provide a reasonable discount on the room prices on weekends and holidays.
3. In the month of January, hotels can start campaigns or marketing with a reasonable amount to increase their revenue as the cancellation is highest in this month.

4. They can also increase the quality of their hotels and their services mainly in Portugal to reduce the cancellation rate.

## About me

### Hi, I'm Ashish!

An aspiring data analyst....

