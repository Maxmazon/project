#include <stdio.h>
#include "cart.h"

void addToCart(CartItem *cart, int *cartCount, int productId, int quantity) {
    if (*cartCount < MAX_CART_ITEMS) {
        cart[*cartCount].product_id = productId;
        cart[*cartCount].quantity = quantity;
        (*cartCount)++;
        printf("Товар додано до корзини!\n");
    } else {
        printf("Не вдалося додати товар до корзини. Максимальна кількість товарів досягнута.\n");
    }
}

void viewCart(CartItem *cart, int cartCount) {
    printf("Корзина:\n");
    for (int i = 0; i < cartCount; i++) {
        int productId = cart[i].product_id;
        int quantity = cart[i].quantity;
        printf("Товар ID: %d, Кількість: %d\n", productId, quantity);
    }
}
