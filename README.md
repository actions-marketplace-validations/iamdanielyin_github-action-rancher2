# github-action-rancher2
>NOTE: only can update image name

### Usage

```yaml
- name: Deploy
  if: success()
  uses: yuyitech/github-action-rancher2@v0.0.1
  env:
    RANCHER_ACCESS_KEY: ${{ secrets.RANCHER_ACCESS_KEY }}
    RANCHER_SECRET_KEY: ${{ secrets.RANCHER_SECRET_KEY }}
    RANCHER_URL: https://xxx.example.com/v3/project/c-xxx:p-xxx/workloads/deployment:default:test
    RANCHER_DATA: |
      [
        {
          "name": "test",
          "image": "registry.cn-hangzhou.aliyuncs.com/xxx/xxx:xxx"
        }
      ]
```

### Parameter Reference
- `api` workload api url
- `access_key` rancher user api keys
- `secret_key` rancher user api keys
- `data` api result's containers field, only support `name` `image` and `environment` field
