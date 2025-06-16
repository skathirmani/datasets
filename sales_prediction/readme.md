
# ML App for Sales Forecasting

You are provided with historical sales data for 1,115 Rossmann stores. Your task is to build a Streamlit web application that forecasts the Sales column in the test data. The app should load a trained machine learning model and allow users to explore and interact with the predictions through a simple, usable interface.

Note: ⚠️ This is not just a model-building exercise. You are expected to build and deploy a working Streamlit app that demonstrates your full-stack skills in data science and application delivery.

### Dataset Files
You will use the following CSV files:
- ```train.csv```: historical data including Sales
- ```test.csv```: historical data excluding Sales
- ```store.csv```: supplemental information about the stores

### Data Field Descriptions
Most of the fields are self-explanatory. The following are descriptions for those that aren't.

- `Id` - an Id that represents a (Store, Date) duple within the test set
- `Store` - a unique Id for each store
- `Sales` - the turnover for any given day (this is what you are predicting)
- `Customers - the number of customers on a given day
- `Open` - an indicator for whether the store was open: 0 = closed, 1 = open
- `StateHoliday` - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None
- `SchoolHoliday` - indicates if the (Store, Date) was affected by the closure of public schools
- `StoreType` - differentiates between 4 different store models: a, b, c, d
- `Assortment` - describes an assortment level: a = basic, b = extra, c = extended
- `CompetitionDistance` - distance in meters to the nearest competitor store
- `CompetitionOpenSince[Month/Year]` - gives the approximate year and month of the time the nearest competitor was opened
- `Promo` - indicates whether a store is running a promo on that day
- `Promo2` - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
- `Promo2Since[Year/Week]` - describes the year and calendar week when the store started participating in Promo2
- `PromoInterval` - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

### Your Deliverables
- Machine Learning Model
  - Train a model to predict the Sales column based on the features provided.
  - Handle missing values, encode categorical variables, and ensure the model generalizes well.
  - Save the trained model using joblib or pickle.

- Streamlit App
  - Create a UI where users can:
    - Upload new test files or select a specific Store and Date to get a prediction.
    - View prediction results in tabular and graphical format.
  - Add visualizations (with filters) to explore sales trends across stores.

- Code file repository
  - Commit the app & model code in your github repository    
