```bash
scripts/setup.sh

docker-compose \
    -f docker-compose-test.yml \
    run --rm unit

docker build -t migspulido/go-demo .

docker tag migspulido/go-demo migspulido/go-demo:1.0

docker tag migspulido/go-demo migspulido/go-demo:1.1

docker push migspulido/go-demo

docker push migspulido/go-demo:1.0

docker push migspulido/go-demo:1.1

docker-compose up -d db app
```
