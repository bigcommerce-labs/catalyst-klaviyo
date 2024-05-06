# Catalyst + Klaviyo

## Getting Started

1. Clone this repository and install its dependencies

```bash
git clone git@github.com:bigcommerce-labs/catalyst-klaviyo.git && cd catalyst-klaviyo && pnpm i
```

2. Copy the environment variable template and enter values for each variable. To help with the BigCommerce variables, you can run the `create-catalyst` CLI's `init` command

```bash
pnpm create @bigcommerce/catalyst@latest init
```

3. The `.env.local` file created by the `init` command above will not create the `NEXT_PUBLIC_KLAVIYO_PUBLIC_KEY` variable, so we'll need to add that. To create a public key, [install and configure the Klaviyo application for BigCommerce](https://help.klaviyo.com/hc/en-us/articles/115005082547). 

> [!NOTE]
> For Step 5 in the Klaviyo help article above, you most likely want to uncheck the **Onsite Tracking** box; onsite tracking scripts are taken care of for you by the files contained in the `integrations/klaviyo` directory at the root of this repository.

4. Now that your Klaviyo account is linked to your BigCommerce store, grab your Klaviyo Public Key from your Klaviyo account: [https://www.klaviyo.com/settings/account/api-keys](https://www.klaviyo.com/settings/account/api-keys), and then run the command below replacing `YOUR_PUBLIC_KEY` with the value retrieved from your account

```bash
echo "NEXT_PUBLIC_KLAVIYO_PUBLIC_KEY=YOUR_PUBLIC_KEY" >> .env.local
```
