# Requirements
## Development server
node version >= v18.13.0
## Deployment
docker
# Usage
## Development server
install project dependencies
```bash
npm install
```
start project 
```bash
npm start
```

## Deployment
1. set API provider by changing `BASENAME_API` constant in `src\lib\constants.js`
2. configure `nginx.conf` file in root directory

3. build docker image

```bash
docker build -t geo-practice .
```

4. start docker container

```bash
docker run -d -p 80:80 geo-practice
```

## Changing API provider
API provider can be changed by setting `BASENAME_API` constant in `src\lib\constants.js`. \
Here is an example of how HTTP-requests are constructed from BASENAME_API: `{BASENAME_API}event/1/query?starttime=2021-10-02T24:00:00&endtime=2021-10-31T23:59:59&limit=100`
