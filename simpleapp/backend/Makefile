moduleowner = github.com/basdemir/simplego/
packagename = simplebackend

# Build And Development
init:
	@ go mod init $(moduleowner)$(packagename)
	@ go mod vendor 
update:
	@ go mod vendor
clean:
	@ sudo rm -rf $(packagename).bin $(packagename).exe cover.txt cover.html cover.out build
run:
	@ go build -o ./build/$(packagename).bin $(moduleowner)$(packagename)/cmd/$(packagename)  && ./build/$(packagename).bin	 
docker: 
	@ docker build -t basdemir/simplego/$(packagename):latest .
docker-push: 
	@ make docker && docker push basdemir/simplego/$(packagename):latest
docker-run: 
	@ docker run -p 8080:8080 basdemir/simplego/$(packagename):latest