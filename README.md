# add-custom-paypal-button-on-cart-drawer-or-page-on-shopify

          # Custom event for drawer Update
          fetch("/cart.js").then((res) => res.json()).then((cart) => {
            console.log("Updated Cart Data:", cart); // Debugging log
            document.dispatchEvent(new CustomEvent("cart:updated", {
              detail: { itemCount: cart.item_count || 0 }
            }));
          });
