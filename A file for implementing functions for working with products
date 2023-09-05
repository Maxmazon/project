#include <stdio.h>
#include <string.h>
#include "product.h"

void addProduct(Product *products, int *productCount, char *name, char *description, float price) {
    if (*productCount < MAX_PRODUCTS) {
        products[*productCount].id = (*productCount) + 1;
        strcpy(products[*productCount].name, name);
        strcpy(products[*productCount].description, description);
        products[*productCount].price = price;
        (*productCount)++;
        printf("Продукт додано!\n");
    } else {
        printf("Не вдалося додати продукт. Максимальна кількість продуктів досягнута.\n");
    }
}

void listProducts(Product *products, int productCount) {
    printf("Список продуктів:\n");
    for (int i = 0; i < productCount; i++) {
        printf("ID: %d\n", products[i].id);
        printf("Назва: %s\n", products[i].name);
        printf("Опис: %s\n", products[i].description);
        printf("Ціна: %.2f\n", products[i].price);
        printf("\n");
    }
}
