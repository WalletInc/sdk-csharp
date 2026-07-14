![Wallet Inc](https://raw.githubusercontent.com/walletinc/sdk-csharp/master/logo.png)

# Wallet SDK for .NET

[![NuGet version](https://img.shields.io/nuget/v/WalletInc.svg?color=2d7ff9)](https://www.nuget.org/packages/WalletInc)
[![NuGet downloads](https://img.shields.io/nuget/dt/WalletInc.svg?color=2d7ff9)](https://www.nuget.org/packages/WalletInc)

The official server-side .NET SDK for the [Wallet Inc](https://wallet.inc) CRM & Digital Payments platform. Create and manage membership tiers, club members, vouchers, promotions, store credit, payment designs, Apple & Google Wallet passes, SMS/MMS, and more.

> **Access note:** this library is currently restricted to Wallet Inc customers. Need access or a hand getting started? Join us on [Discord](https://discord.gg/xzwhcNCjcQ).

## Links

- Website: https://wallet.inc
- Developer docs: https://wallet.dev
- API status: https://uptime.wallet.inc
- All SDKs: https://github.com/walletinc

## Requirements

.NET 8.0 or later.

## Installation

```bash
dotnet add package WalletInc
```

Or via the Package Manager Console:

```powershell
Install-Package WalletInc
```

## Quickstart

Point the client at the API host and send your API key as the `access-token` header on every request. Create your key in the [Wallet Developer Hub](https://wallet.dev).

```csharp
using WalletInc.Api;
using WalletInc.Client;
using WalletInc.Model;

var config = new Configuration
{
    BasePath = "https://api.wall.et"
};
// Send your API key as the access-token header on every request.
config.DefaultHeaders.Add("access-token", "YOUR_API_KEY");

var membershipTiers = new MembershipTiersApi(new HttpClient(), config, new HttpClientHandler());

var tier = membershipTiers.CreateMembershipTier(
    new WTMembershipTierCreationParams(tierNumber: "1", tierName: "GOLD", tierDiscount: 20f)
);

Console.WriteLine(tier);
```

## Documentation

Full API reference and guides live in the [Wallet Developer Hub](https://wallet.dev). Per-endpoint method docs and model definitions for this client are generated into the [`docs/`](docs/) folder of this repository.

## About Wallet Inc

[Wallet Inc](https://wallet.inc) is a CRM and digital payments platform: digital membership cards, loyalty and rewards, vouchers and store credit, Apple & Google Wallet passes, and SMS/MMS marketing. Learn more at [wallet.inc](https://wallet.inc) and explore the APIs at the [Wallet Developer Hub](https://wallet.dev).

## License

Proprietary. Use of this SDK is governed by the Wallet Inc terms at [wallet.law](https://wallet.law).
