# VirtueMart - Mercado Pago Module (v3.0.x)

* [Features](#features)
* [Available versions](#available_versions)
* [Installation](#installation)
* [Standard Checkout Configuration](#configuration_std)
* [Credit Card - Custom Checkout Configurationn](#configuration_custom)
* [Ticket - Custom Checkout Configuration](#configuration_custom_ticket)
* [Feedback](#feedback)

<a name="features"></a>
##Features##

**Credit Card Customized Checkout**

This feature will allow merchants to have a customized checkout for credit card
payment. Thus, it will be possible to customize its look and feel, customers won’t be
redirected away to complete the payment, and it will also reduce the checkout steps
improving conversion rates.

*Available for Argentina, Brazil, Colombia, Mexico and Venezuela*

**Ticket Checkout**

This feature allows merchants to have a customized bar code payment. It
reduces the checkout steps improving conversion rates. The bar code payment will
have merchant's logo.

*Available for Argentina, Brazil, Colombia, Mexico and Venezuela*

**OneClick Pay (Customer & Cards)**
This feature allows to store credit card information for the customer, so that the next time there is no need to enter all the card details. Customers will just need to re-enter the security code of the credit card they want to use.

**Standard checkout**

This feature allows merchants to have a standard checkout. It includes features like
customizations of title, description, category, and external reference, integrations via
iframe, modal, and redirection, with configurable auto-returning, max installments and
payment method exclusion setup, and sandbox/debug options.

*Available for Argentina, Brazil, Chile, Colombia, Mexico, Peru and Venezuela*

<a name="available_versions"></a>
##Available versions##
<table>
  <thead>
    <tr>
      <th>Plugin Version</th>
      <th>Status</th>
      <th>VirtueMart Compatible Versions</th>
    </tr>
  <thead>
  <tbody>
    <tr>
      <td>v2.0.2</td>
      <td>Stable (Current version)</td>
      <td>VirtueMart v3.0.x</td>
    </tr>
  </tbody>
</table>

<a name="installation"></a>
##Installation##

1. Download the zip module
2. Go to **Extensions > Extension Manager**
3. In **Upload Package File > Package File** select the **cart-virtuemart.zip** and click **Upload & Installation**

<a name="configuration_std"></a>
##Standard Checkout Configuration##

1. Go to **VirtueMart > Payment Methods** and click **New**

2. Complete the fields:
  - **Payment Name** set **Mercado Pago**
  - **Sef Alias** set **mercadopago**
  - **Payment Method** select **Mercado Pago**
  - **Published** set to **true**
3. Click in **Save**

4. Go to **Configuration** tab <br/>
  First of all, you need to configure your client credentials. To make it, fill your **Client_id** and **Client_secret** in Credentials Configuration section.

  ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/credentials.png) <br />

  You can obtain your **Client_id** and **Client_secret**, accordingly to your country, in the following links:

  * Argentina: https://www.mercadopago.com/mla/herramientas/aplicaciones
  * Brazil: https://www.mercadopago.com/mlb/ferramentas/aplicacoes
  * Chile: https://www.mercadopago.com/mlc/herramientas/aplicaciones
  * Colombia: https://www.mercadopago.com/mco/herramientas/aplicaciones
  * Mexico: https://www.mercadopago.com/mlm/herramientas/aplicaciones
  * Peru: https://www.mercadopago.com/mpe/account/credentials?type=basic
  * Venezuela: https://www.mercadopago.com/mlv/herramientas/aplicaciones

5. Checkout settings. <br/>

  ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/checkout_settings.png) <br />

  **Type Checkout**: How your customers will interact with Mercado Pago to pay their orders;<br />
  **Auto Redirect**: If set, the platform will return to your store when the payment is approved.<br />
  **Maximum Number of Installments**: The maximum installments allowed for your customers;<br />
  **Exclude Payment Methods**: Select the payment methods that you want to not work with Mercado Pago.<br />
  **iFrame Width**: The width, in pixels, of the iFrame (used only with iFrame Integration Method);<br />
  **iFrame Height**: The height, in pixels, of the iFrame (used only with iFrame Integration Method);<br />
  **Mercado Pago Sandbox**: Test your payments in Mercado Pago sandbox environment;<br/>

6. IPN settings. <br/>

  ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/ipn_settings.png) <br />

  * **Choose the status of approved orders**: Sets up the order status when payments are approved.
  * **Choose the status when payment is pending**: Sets up the order status when payments are pending.
  * **Choose the status when payment is process**: Sets up the order status when payments are in process.
  * **Choose the status when client open a mediation**: Sets up the order status when client opens a mediation.
  * **Choose the status of refunded orders**: Sets up the order status when payments are refunded.
  * **Choose the status when payment was chargeback**: Sets up the order status when payments are chargeback.
  * **Choose the status when payment was canceled**: Sets up the order status when payments are canceled.
  * **Choose the status when payment was reject**: Sets up the order status when payments are rejected.

7. Other settings. <br/>

  ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/other_settings.png) <br />

  **Store Category**: Sets up the category of the store;<br />
  **Log**: Enables/disables logs.<br />
  **Logo**: Select the logo. You must add the file in the folder /images/stories/virtuemart/payment <br />

<a name="configuration_custom"></a>
##Credit Card - Custom Checkout Configuration##

  1. Go to **VirtueMart > Payment Methods** and click **New**

  2. Complete the fields:
    - **Payment Name** set **Credit Card - Mercado Pago**
    - **Sef Alias** set **mercadopago**
    - **Payment Method** select **Mercado Pago**
    - **Published** set to **true**

  3. Click in **Save**

  4. Go to **Configuration** tab

  5. On **Mercado Pago Product** select **Credit Card - Checkout Custom**

  6. Now configure your credentials. To make it, fill your **access_token** in Credentials Configuration section.

    ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/credentials_custom.png) <br />

    You can obtain your **Public Key** and **Access Token**, accordingly to your country, in the following links:

    * Argentina: https://www.mercadopago.com/mla/account/credentials
    * Brazil: https://www.mercadopago.com/mlb/account/credentials
    * Colombia: https://www.mercadopago.com/mco/account/credentials
    * Mexico: https://www.mercadopago.com/mlm/account/credentials
    * Venezuela: https://www.mercadopago.com/mlv/account/credentials

  7. Checkout settings. <br/>

    ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/checkout_settings_custom.png) <br />

    **Statement Descriptor**: Sets the label as the customer will see the charge for amount in his/her bill;<br />
    **Binary**: When set to true, the payment can only be approved or rejected. Otherwise in_process status is added.<br />

  8. IPN settings. <br/>

    ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/ipn_settings.png) <br />

    * **Choose the status of approved orders**: Sets up the order status when payments are approved.
    * **Choose the status when payment is pending**: Sets up the order status when payments are pending.
    * **Choose the status when payment is process**: Sets up the order status when payments are in process.
    * **Choose the status when client open a mediation**: Sets up the order status when client opens a mediation.
    * **Choose the status of refunded orders**: Sets up the order status when payments are refunded.
    * **Choose the status when payment was chargeback**: Sets up the order status when payments are chargeback.
    * **Choose the status when payment was canceled**: Sets up the order status when payments are canceled.
    * **Choose the status when payment was reject**: Sets up the order status when payments are rejected.

<a name="configuration_custom_ticket"></a>
##Ticket - Custom Checkout Configuration##

  1. Go to **VirtueMart > Payment Methods** and click **New**

  2. Complete the fields:
    - **Payment Name** set **Ticket - Mercado Pago**
    - **Sef Alias** set **mercadopago**
    - **Payment Method** select **Mercado Pago**
    - **Published** set to **true**

  3. Click in **Save**

  4. Go to **Configuration** tab

  5. On **Mercado Pago Product** select **Ticket - Checkout Custom**

  6. Now configure your credentials. To make it, fill your **public_key** and **access_token** in Credentials Configuration section.

    ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/credentials_custom_ticket.png) <br />

    You can obtain your **Access Token**, accordingly to your country, in the following links:

    * Argentina: https://www.mercadopago.com/mla/account/credentials
    * Brazil: https://www.mercadopago.com/mlb/account/credentials
    * Colombia: https://www.mercadopago.com/mco/account/credentials
    * Mexico: https://www.mercadopago.com/mlm/account/credentials
    * Venezuela: https://www.mercadopago.com/mlv/account/credentials

  7. IPN settings. <br/>

    ![Installation Instructions](https://raw.github.com/mercadopago/cart-virtuemart/master/README.img/ipn_settings.png) <br />

    * **Choose the status of approved orders**: Sets up the order status when payments are approved.
    * **Choose the status when payment is pending**: Sets up the order status when payments are pending.
    * **Choose the status when payment is process**: Sets up the order status when payments are in process.
    * **Choose the status when client open a mediation**: Sets up the order status when client opens a mediation.
    * **Choose the status of refunded orders**: Sets up the order status when payments are refunded.
    * **Choose the status when payment was chargeback**: Sets up the order status when payments are chargeback.
    * **Choose the status when payment was canceled**: Sets up the order status when payments are canceled.
    * **Choose the status when payment was reject**: Sets up the order status when payments are rejected.

<a name="feedback"></a>
##Feedback##

  We want to know your opinion, please answer the following form.
  <ul>
  	<li><a href="http://goo.gl/forms/2n5jWHaQbfEtdy0E2" target="_blank">Portuguese</a></li>
  	<li><a href="http://goo.gl/forms/A9bm8WuqTIZ89MI22" target="_blank">Spanish</a></li>
  </ul>
