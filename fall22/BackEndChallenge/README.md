# 2022-23 Interview Back-End Challenge (Fall)

On the Autonomous Intelligent Vehicle (AIV) team at Martinrea Alfield, you will be tasked with implementing various web applications that will be used by a diverse cast of stakeholders. One of these applications is the AIV list service. The AIV list service allows AIV front-end app developers to retrieve a list of online AIVs in the factory.

You are responsible for implementing the AIV list service in any language or web framework of your choice.

An AIV-type object has the following structure:
```
AIV := {
    id: <INT>,
    name: <STRING>,
    online: <BOOLEAN>,
}
```

The list AIV service should be a `GET` endpoint on the url `/api/AIVList`. It has the following requirements:
- The service should return responses in the `application/json` format
- If the HTTP header `X-API-KEY` is not set, or is set to anything other than `123secret`, return a response with HTTP status code `403` - forbidden (no response data is necessary)
- Conversely, if the `X-API-KEY` is correct, return a response with HTTP status code `200` - OK, with the response data being a JSON representation of the AIVs stored in the system

**Note: It is totally fine to hardcode the list of AIVs in the system (just make up some example AIVs).**

**Another note: Showing your system working would be worth bonus points, but it's fine if you don't write any test cases or run any tests.**

**A FINAL note: Feel free to use any documentation or internet resources that help you.**

