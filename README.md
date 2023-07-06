#  Optimizely API

Tagging a release on this repository will update the Python SDK.

## What is in this repository?

This repository contains

- Optimizely's OpenAPI spec which lives in the [openapi](./fern/api/openapi/) folder
- Generators (see [generators.yml](./fern/api/generators.yml))

To make sure that the OpenAPI is valid, you can use the Fern CLI.

```bash
npm install -g fern-api
fern check
```

## What are generators?

Generators read in your API Definition and output artifacts (e.g. ) and are tracked in [generators.yml](./fern/api/generators.yml).

To trigger the generators run:

```bash
fern generate

fern generate --group publish --version <version>
```

The publish command currently runs in a GitHub workflow (see [ci.yml](.github/workflows/ci.yml)). To trigger the generators using Github Actions:

### 1. Click on Releases
![Step 1 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/23133ef3-c887-4924-ae33-606dbda09c48/33baf2dc-5e15-40b1-8638-aaff968e21b9.png?crop=focalpoint&fit=crop&fp-x=0.6875&fp-y=0.7150&fp-z=2.3638&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=505&mark-y=575&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz0zNDkmaD05NCZmaXQ9Y3JvcCZjb3JuZXItcmFkaXVzPTEw)


### 2. Click on Draft a new release
![Step 2 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/4819009c-21bb-458b-9e08-171c25f3c3a8/63ef387f-1fdc-4c9e-9213-4717fb0fef25.png?crop=focalpoint&fit=crop&fp-x=0.5167&fp-y=0.2838&fp-z=2.0000&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=510&mark-y=301&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz00OTQmaD0xMTcmZml0PWNyb3AmY29ybmVyLXJhZGl1cz0xMA%3D%3D)


### 3. Click on Choose a tag
![Step 3 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/737446b0-abc4-4b97-925e-2319368d4bae/cf67865b-e4d5-419d-ae42-77533616dbf6.png?crop=focalpoint&fit=crop&fp-x=0.1289&fp-y=0.3479&fp-z=1.9641&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=57&mark-y=396&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz00OTMmaD0xMTUmZml0PWNyb3AmY29ybmVyLXJhZGl1cz0xMA%3D%3D)


### 4. Specify a version
This version string is used when publishing SDKs to registries (e.g. npm, maven).
![Step 4 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/7e039623-bd85-48d5-8e94-343be622e529/4f8778d8-7b50-48ef-bf7c-bda79cb89cbf.png?crop=focalpoint&fit=crop&fp-x=0.2118&fp-y=0.4800&fp-z=1.5323&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=65&mark-y=408&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz02NDgmaD04OSZmaXQ9Y3JvcCZjb3JuZXItcmFkaXVzPTEw)


### 5. In the title, re-enter the version number
![Step 5 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/cee2c4f7-964d-46f8-878a-c0f72aebcc5a/96fe8032-3d60-4c06-9cb7-640e174b2485.png?crop=focalpoint&fit=crop&fp-x=0.2967&fp-y=0.4659&fp-z=1.1838&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=35&mark-y=418&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz03NzQmaD02OSZmaXQ9Y3JvcCZjb3JuZXItcmFkaXVzPTEw)


### 6. Click on Publish release
![Step 6 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/cafbdfbd-736b-416e-aae9-aadd9a110621/fcf2b74a-e787-49ef-a26f-3789d25da5e7.png?crop=focalpoint&fit=crop&fp-x=0.2011&fp-y=0.7601&fp-z=2.1157&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=62&mark-y=537&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz00MzgmaD0xMjMmZml0PWNyb3AmY29ybmVyLXJhZGl1cz0xMA%3D%3D)


### 7. Click on Actions
See the Actions that will run `fern generate`.
![Step 7 screenshot](https://images.tango.us/workflows/ec2c605b-fc43-40dd-890c-57a738cd7571/steps/1a41be0f-7860-46ad-80f3-eb75b40d5a89/27d92e40-b3f6-4aa6-9f09-47b8a8c6209a.png?crop=focalpoint&fit=crop&fp-x=0.4518&fp-y=0.1292&fp-z=2.3774&w=1200&border=2%2CF4F2F7&border-radius=8%2C8%2C8%2C8&border-radius-inner=8%2C8%2C8%2C8&blend-align=bottom&blend-mode=normal&blend-x=0&blend-w=1200&blend64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL21hZGUtd2l0aC10YW5nby13YXRlcm1hcmstdjIucG5n&mark-x=428&mark-y=212&m64=aHR0cHM6Ly9pbWFnZXMudGFuZ28udXMvc3RhdGljL2JsYW5rLnBuZz9tYXNrPWNvcm5lcnMmYm9yZGVyPTYlMkNGRjc0NDImdz0zNDQmaD0xMzImZml0PWNyb3AmY29ybmVyLXJhZGl1cz0xMA%3D%3D)

<br/>

***
