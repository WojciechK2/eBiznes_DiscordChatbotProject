# eBiznes_DiscordChatbotProject  
A docker composed container for DiscordBot  

Separate fragments are located:  
Discord_Client: https://github.com/WojciechK2/Discord_proxy_client  
Simple KTOR Backend: https://github.com/WojciechK2/eBiznes_Project_Simple_Backend  

Ktor based backend with Exposed ORM.   
CRUD-like communication and resource management.   
Ktor based client for proxying requests to a backend.  

1. add the .env file in the Discord_Client folder (path should match "Discord_Client/.env")  
	SERVER_URL=http://backend:8080/  
	DISCORD_TOKEN=<your token>    
2. 
	docker compose up  
3.
	check the bot on the Discord server you added it in  
4.
	Ping bot by mentioning it in added Guild @\<KTORBOTNAME\> \<command\>  

Help Page  
	type help for help  
	
	Asking for products: message me "products",  
	Asking for categories: message me "categories"  
	Asking for specific product: message me "products "  
	Asking for specific category: message me "categories "  
