 !!!plain
                _                                 ___
               ( )_                             /'___)_
    _ _  _   _ | ,_)   _      ___    _     ___ | (__ (_)   __
  /'_` )( ) ( )| |   /'_`\  /'___) /'_`\ /' _ `\ ,__)| | /'_ `\
 ( (_| || (_) || |_ ( (_) )( (___ ( (_) )| ( ) | |   | |( (_) |
 `\__,_)`\___/'`\__)`\___/'`\____)`\___/'(_) (_)_)   (_)`\__  |
                                                        ( )_) |
                                                         \___/'

## What is it

Autoconfig in an automated way to create flexible configuration structures representing your YAML configuration

## How does it work

1. require 'autoconfig'
2. profit!

## Example

Lets say you have application.yml in your config folder:

  !!!plain
  defaults:
	  web:
		  hostname: 'localhost'
    noreply: noreply@myhost.com
	  support_email: support@myhost.com
  production:
	  web:
		  hostname: "the.production.com"

After requiring 'autoconfig' you should expect ApplicationConfig structure that will contain all the information. In production environment
ApplicationConfig.web.hostname call will return "the.production.com".

## Configuration

By default, it will look at config directory of your project and transfer most of your .yml files (it ignores database ones). However,
you have full control over where it need to look and what to convert.
