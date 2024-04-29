# Notes

Build a Full-Stack React Application ([AWS Resource Center](https://aws.amazon.com/getting-started/hands-on/build-react-app-amplify-graphql/)).

## Amplify v5 versus v6

The tutorial is based on Amplify v5. Today, Amplify v6 is the standard which means that some code adjustments are required. This affects the GraphQL and Storage component. AWS no longer export the API class, but instead have a `generateClient()` export to set up a client to make the calls.

## Disable self sign-up

### Hide sign-up form (frontend)

```javascript
//export default withAuthenticator(App);
export default withAuthenticator(App, { hideSignUp: true });
```

### Disable self-registration (Amazon Cognito)

Amazon Cognito -> User pools -> ... -> Sign-up experience -> Self-service sign-up -> Edit

**Disable** self-registration.

### Resources

- <https://github.com/aws-amplify/amplify-js/issues/6089>
