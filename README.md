##Overview
This project demonstrates the **Sustainsy.Saml2** library, which adds SAML2P support to ASP.NET web sites, allowing the web site to act as a SAML2 Service Provider.

It uses the Sustainsys notional Identity Provider (IDP), which can be a stand-in replacement for testing purposes.

Follow the directions on the Systainsys site to configure your ASP.NET app: https://saml2.sustainsys.com/en/2.0/configuration.html

## In Brief:
- Most modifications will be in your Web.config file
- Configure the ReturnURL in the "sustainsys.saml2 ..." Web.config section. It's set by default to localhost, which is appropriate for testing locally.
- Add a reference to Sustainsys.Sanl2.Mvc
- In the controller for the Return-URL, cast the Current.User.Identity to ClaimsIdentity to have access to the user's claims via the ClaimsIdentity's Claims enumeration