# Accounts

This is account management API

[http://api-new.quantforce.net/swagger/index.html](http://api-new.quantforce.net/swagger/index.html)

You can list/create/update accounts

You can create as many account as you need. An account can contains account \(recursive\).

This allow you to manage all the accounts like you use to do.

You have a tag propertie where you can put what you want.

```C#
public class AccountModel
    {
        /// <summary>
        /// Quantforce Id
        /// </summary>
        public string _id { get; set; }

        /// <summary>
        /// Parent id
        /// </summary>
        public string qfIdParent { get; set; }

        /// <summary>
        /// User subscriptionKey
        /// </summary>
        public string subscriptionKey { get; set; }

        /// <summary>
        /// User name
        /// </summary>
        public string name { get; set; }

        /// <summary>
        /// Mail address
        /// </summary>
        public string mail { get; set; }

        /// <summary>
        /// Free to use value
        /// </summary>
        public string tag { get; set; }

        /// <summary>
        /// Send the invoice from this account and all is childs
        /// </summary>
        public bool invoice { get; set; }

        /// <summary>
        /// Bank infos
        /// </summary>
        public string iban { get; set; }
    }
```



