import requests  

def get_crypto_data(crypto_id):  
    url = f"https://api.coingecko.com/api/v3/simple/price?ids={crypto_id}&vs_currencies=usd&include_market_cap=true&include_24hr_change=true"  
    
    try:  
        response = requests.get(url)  
        data = response.json()  
        
        # Check if data was retrieved  
        if crypto_id in data:  
            price = data[crypto_id]['usd']  
            market_cap = data[crypto_id]['usd_market_cap']  
            price_change_24h = data[crypto_id]['usd_24h_change']  
            
            print(f"Cryptocurrency: {crypto_id.capitalize()}")  
            print(f"Current Price (USD): ${price:.2f}")  
            print(f"Market Cap (USD): ${market_cap:,.2f}")  
            print(f"24h Price Change: {price_change_24h:.2f}%")  
        else:  
            print("Cryptocurrency not found.")  
    
    except requests.exceptions.RequestException as e:  
        print(f"Error retrieving data: {e}")  

if __name__ == "__main__":  
    # Example cryptocurrency ID, can be changed to others like 'bitcoin', 'ethereum', etc.  
    print("Bitcoin Today")
    print(" ")
    crypto_id = 'bitcoin'  
    get_crypto_data(crypto_id)

    print(" ")

    print("Ethereum Today")
    print(" ")
    crypto_eth = 'ethereum'  
    get_crypto_data(crypto_eth)  

    print("")
    print("Ripple Today")
    print("")
    crypto_ripple = 'ripple'
    get_crypto_data(crypto_ripple)
