# Hubspot API wrapper in Elixir

[![Hex.pm](https://img.shields.io/hexpm/v/hubspotex.svg?maxAge=2592000)](https://hex.pm/packages/hubspotex)
 [![Hex.pm](https://img.shields.io/hexpm/l/hubspotex.svg?maxAge=2592000)](https://hex.pm/packages/hubspotex)
 [![Hex.pm](https://img.shields.io/hexpm/dt/hubspotex.svg?maxAge=2592000)](https://hex.pm/packages/hubspotex)
 [![Build Status](https://travis-ci.org/ryanwinchester/hubspotex.svg?branch=master)](https://travis-ci.org/ryanwinchester/hubspotex)


[[Hex]](https://hex.pm/packages/hubspotex) [[Docs]](https://hexdocs.pm/hubspotex/api-reference.html)

## Examples

```elixir

Hubspot.Contacts.all
#=> %Hubspot.HTTP.Request{endpoint: "/contacts/v1/lists/all/contacts/all",
#     method: :get, query: [], body: ""}

Hubspot.Contacts.all |> Hubspot.request
#=> {:ok, response}

Hubspot.Contacts.all([count: 10, vidOffset: 100]) |> Hubspot.request
#=> {:ok, response}
```

## Installation

To install the released version [available in Hex](https://hex.pm/docs/publish), the package can be installed by adding hubspotex to your list of dependencies in `mix.exs`:

  ```elixir
  def deps do
    [{:hubspotex, "~> 0.0.6"}]
  end
  ```

To install the latest master from a github branch, the package can be installed by adding hubspotex to your list of dependencies in `mix.exs`:

  ```elixir
  def deps do
    [{:hubspotex, github: "tmaszk/hubspotex" }]
  end
  ```

## Config


Configure your credentials in `config.exs`, `prod.exs`, or `runtime.exs` depending on your deployment method.  Get the values from [HubSpot account](https://app.hubspot.com/myaccounts).

  ```elixir
  import Config

  config :hubspotex, auth_method: "hapikey" # "hapikey" or "token"
  config :hubspotex, auth_key: "demo"
  config :hubspotex, portal_id: "62515"
  config :hubspotex, username: "testapi@hubspot.com"
  config :hubspotex, password: "HubSpot"
  ```
