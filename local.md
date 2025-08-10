```bash
docker compose up -d
docker compose exec cuda-dev bash
nvcc my_kernel.cu -o my_kernel
```