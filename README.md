# LaunchDarkly Sample Client-Side Node.js Application

## Description

This is a sample application that uses the LaunchDarkly Node.js client-side SDK. The feature flag used in this test is named `enable-toggle-runner`, this feature flag if enabled or disabled will display in the console when the application is run. The use of targeting is also displayed in the application and the LaunchDarkly dashboard, targeting the user by the key `example-user-key`.

## Pre-requisites

Please have a LaunchDarkly account or sign up for a trial here(https://launchdarkly.com/start-trial/)

## LaunchDarkly Application Set Up

1. Sign up for a free trial or log into your existing LaunchDarkly account

2. Set up a new environment with any name

3. Select the node client SDK called Node.js (Client)

4. Create a Feature Flag named `Enable Toggle Runner`

5. Clone this repository 

6. Follow instructions in the Build Instructions section below

## Build Instructions

1. Install the LaunchDarkly Client-Side Node.js SDK by running `npm install`

2. Edit `index.js` and set the value of `environmentId` to your LaunchDarkly client-side ID. The example feature flag will already be set.

```js
  const environmentId = "1234567890abcdef";

  const featureFlagKey = "enable-toggle-runner";
```

3. Run `node index.js`

You should see the message `"Feature flag '<flag key>' is <true/false> for this user"`.

4. If you would like to test enabling/disabling this flag within the LaunchDarkly application go to the 'Feature Flags' section in the application and then select the `enable-toggle-runner` feature flag and then toggle the switch on or off

## Targeting

We display the use of user targeting within the sample application. To test this go to the details of the the `enable-toggle-runner` by clicking on the name. 

To target the example user toggle the switch for `Targeting` and add the example user key supplied in the sample appilcation to the `true` list of users. Example user key `example-user-key`, once you see the user name populate click `Review and Save` in the top right of the page. Run the application and you should see `*** Feature flag 'enable-toggle-runner' is true for this user`