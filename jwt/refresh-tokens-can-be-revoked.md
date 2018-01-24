# Refresh tokens can be revoked

The purpose of a refresh token is to refresh an expired JavaScript web token. So instead of setting a high TTL (time to live) value for the JWT it's set to a small duration such as 15 minutes. You have to keep in mind, that an JWT can not be revoked. The refresh token on the other hand can be revoked. Often it's saved as database record. So for example if a logout is issued the refresh token will be revoked and the JWT expires shortly after. That way a leaked token has no access rights anymore.