# golang-blockchain
Mimics a book borrowing ledger on a blockchain

Requirements:
1. Install <a href="https://go.dev/doc/install">golang</a>.
2. Install <a href="https://www.postman.com/downloads/">postman</a>.

To Deploy:

1. Clone this repo.
2. In the repo directory run 'go run main.go'.

This diplays the genesis block of the blockchain.
<p align="center"><img src="https://drive.google.com/uc?export=view&id=18vbKaXq6cn7Tz42sLeb6nv43fe1aaFwm" alt="genesis-block"></p>

To create a new book:

1. Open postman.
2. Create a post request to 'http://localhost:3000/new'.
3. Body of the post request is raw. {"title": "Harry Potter", "author":"Rowling","isbn":"999","publish_date":"2000-05-26"}
4. Send request.

The response should be something like below:
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1RaT9i7yPwVYxySE5p5dkMbRxtXyVyJhP" alt="genesis-block"></p>

To borrow a book:

1. Use the id of the book from the response above.
2. Create a post request to 'http://localhost:3000'.
3. Body of the post request is raw. {"book_id": id-from-above, "user": "ABC", "checkout_date":"2023-05-28"}
4. Post request. 

The response should be something like below:
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1_ghIAA2c4nAuAeKKGcNDB_3Q58CpEtfh" alt="genesis-block"></p>

To check the state of the chain:

1. Create a get request to 'http://localhost:3000'.
2. Send request.

The response should be something like below:
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1OlESqg3UA--Q5QFFYdsY6F115mw7eBo-" alt="genesis-block"></p>

