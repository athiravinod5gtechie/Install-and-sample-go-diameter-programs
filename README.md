# Install-and-sample-go-diameter-programs 
# Ref : https://github.com/panyogesh/integration-magma/blob/main/utils/go-diameter-sample.md
# Install go language 

sudo apt-get update 

sudo apt-get -y upgrade 

sudo snap install go –classic 

go version 

Add following line in profile 

		export PATH=$PATH:/usr/local/go/bin 

source ~/.profile 

# Get the go-diameter package 

git clone https://github.com/fiorix/go-diameter.git 

cd go-diameter/ 

# Run go-diameter Client/Server program 

cd go-diameter/examples  

[Terminal 1] go build server/server.go 

[Terminal 2] go build client/client.go 

[Terminal 1] ./server 

[Terminal 2] ./client 

[Terminal 1] ./server 

[Terminal 2] ./client -hello 

# Run go-diameter s6a_Client/s6a_Server program 

cd go-diameter/examples/ s6a_server 

[Terminal 1] ./server 

cd go-diameter/examples/ s6a_client 

[Terminal 2] ./main -addr 127.0.0.1:3868 -network_type tcp 

# Run the test on s6a_proxy 

cd go-diameter/examples/s6a_proxy/service/test 

go test 

 
