
# Upgrading System

sudo apt update -y && 
sudo apt upgrade -y

# Install Node.js and npm
sudo apt install nodejs -y && 
sudo apt install npm -y && 
sudo npm install -g serve pm2

# Cloing Git Repo
git clone https://github.com/MuhammadTaimoorAnwar511/shop.git 
# Backend
cd server
npm i
npm run dev
or
pm2 start index.js --name grocery-backend
cd ..
# Frontend
cd client
npm i
npm run dev -- --host 0.0.0.0
or
pm2 start serve-client.mjs --interpreter node --name grocery-client
edit
client/src/pages/seller/ProductList.jsx->src={`http://localhost:5000/images/${product.image[0]}`}
