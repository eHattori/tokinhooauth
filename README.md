# TOKINHO OAUTH 2 AUTH0

These samples demonstrate how to create an API with Django which only permits access to resources if a valid access token is included. This verification is done by validating the signature and claims in a JSON Web Token (JWT) signed by Auth0.

## Install
```
pip install -r requirements.txt
```

## Run
```
python manage.py runserver 8000
```

## Testing the API
You can then try to do a GET to http://localhost:8000/api/private which will throw an error if you don't send an access token signed with RS256 with the appropriate issuer and audience in the Authorization header.

You can also try to do a GET to http://localhost:8000/api/private-scoped/ which will throw an error if you don't send an access token with the scope read:messages signed with RS256 with the appropriate issuer and audience in the Authorization header.