# Smart-Mirror

# Download config.json file

/* Magic Mirror Config Sample

 *

 * By Michael Teeuw https://michaelteeuw.nl

 * MIT Licensed.

 *

 * For more information on how you can configure this file

 * see https://docs.magicmirror.builders/getting-started/configuration.html#general

 * and https://docs.magicmirror.builders/modules/configuration.html

 */

let config = {

	address: "0.0.0.0", 	// Address to listen on, can be:
							// - "localhost", "127.0.0.1", "::1" to listen on loopback interface
							// - another specific IPv4/6 to listen on a specific interface
							// - "0.0.0.0", "::" to listen on any interface
							// Default, when address config is left out or empty, is "localhost"
	electronOptions: {
			webPreferences: {
				webviewTag: true
			}
		},
	port: 8569,
	basePath: "/", 	// The URL path where MagicMirror is hosted. If you are using a Reverse proxy
					// you must set the sub path here. basePath must end with a /
	ipWhitelist:[], 	// Set [] to allow all IP addresses
															// or add a specific IPv4 of 192.168.1.5 :
															// ["127.0.0.1", "::ffff:127.0.0.1", "::1", "::ffff:192.168.1.5"],
															// or IPv4 range of 192.168.3.0 --> 192.168.3.15 use CIDR format :
															// ["127.0.0.1", "::ffff:127.0.0.1", "::1", "::ffff:192.168.3.0/28"],

 
	useHttps: false, 		// Support HTTPS or not, default "false" will use HTTP
	httpsPrivateKey: "", 	// HTTPS private key path, only require when useHttps is true
	httpsCertificate: "", 	// HTTPS Certificate path, only require when useHttps is true

	language: "ko",
	locale: "en-US",
	logLevel: ["INFO", "LOG", "WARN", "ERROR"], // Add "DEBUG" for even more logging
	timeFormat: 24,
	units: "metric",
	// serverOnly:  true/false/"local" ,
	// local for armv6l processors, default
	//   starts serveronly and then starts chrome browser
	// false, default for all NON-armv6l devices
	// true, force serveronly mode, because you want to.. no UI on this device

	modules: [

		{
	module: "MMM-Jast",
	position: "top_bar",
	config: {

		maxWidth: "100%",
		updateIntervalInSeconds: 500,
		fadeSpeedInSeconds: 150,
		scroll: "horizontal", // One of ["none", "vertical", "horizontal"]
		useGrouping: false,
		currencyStyle: "code", // One of ["code", "symbol", "name"]
		lastUpdateFormat: "HH:mm",
		showColors: true,
		showCurrency: true,
		showChangePercent: true,
		showChangeValue: false,
		showChangeValueCurrency: false,
		showLastUpdate: false,
		showPortfolioValue: false,
		showPortfolioGrowthPercent: false,
		showPortfolioGrowth: false,
		numberDecimalsValues: 2,
		numberDecimalsPercentages: 1,
		virtualHorizontalMultiplier: 2,

		stocks: [
			{ name: "BASF", symbol: "BAS.DE", quantity: 10 },
			{ name: "SAP", symbol: "SAP.DE", quantity: 15 },
			{ name: "Henkel", symbol: "HEN3.DE" },
			{ name: "Alibaba", symbol: "BABA"},
			{ name: "Tesla", symbol: "TSLA"},
			{ name: "Alphbet(GOOG)", symbol: "GOOG"},
			{ name: "Amazon", symbol: "AMZN"},
			{ name: "Apple", symbol: "AAPL"},
			{ name: "Microsoft", symbol: "MSFT"},
			{ name: "Taiwan Semiconductor TSMC", symbol: "2330.TW"},
			{ name: "ASML Holding" , symbol: "ASML"},
			{ name: "NVIDIA Corp", symbol: "NVDA"},
			{ name: "Intel Corp", symbol: "INTC"}
		]
	}
},
.
.
.
.
.
.
![구글전](https://user-images.githubusercontent.com/101620585/165213262-d0d0ebc0-0a81-4ee0-a585-208e30edf106.png)
![구글후](https://user-images.githubusercontent.com/101620585/165213275-1b1fedc2-1bb9-49b4-bbe2-8530988d2384.png)
