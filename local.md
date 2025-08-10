```bash
# can only compile on docker container
docker compose up -d
docker compose exec cuda-dev bash


# vast.ai: compile and run on remote server
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
ssh -i ~/.ssh/vast_ai -p 54480 root@<your_vast_ip> -L 8080:localhost:8080
scp -i ~/.ssh/vast_ai -P 54480 ./main.cu root@<your_vast_ip>:/workspace/main.cu
nvcc main.cu -o main
./main
```