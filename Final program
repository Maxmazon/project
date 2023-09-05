#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_PRODUCTS 100
#define MAX_NAME_LENGTH 50
#define MAX_DESCRIPTION_LENGTH 200
#define MAX_CART_ITEMS 10

// Structure to represent a product
typedef struct {
    int id;
    char name[MAX_NAME_LENGTH];
    char description[MAX_DESCRIPTION_LENGTH];
    float price;
} Product;

// Structure to represent a shopping cart item
typedef struct {
    int product_id;
    int quantity;
} CartItem;

// Global variables
Product products[MAX_PRODUCTS];
int productCount = 0;
CartItem cart[MAX_CART_ITEMS];
int cartCount = 0;

// Add a product
void addProduct(char *name, char *description, float price) {
    if (productCount < MAX_PRODUCTS) {
        products[productCount].id = productCount + 1;
        strcpy(products[productCount].name, name);
        strcpy(products[productCount].description, description);
        products[productCount].price = price;
        productCount++;
        printf("Product added!\n");
    } else {
        printf("Unable to add product. Maximum number of products reached.\n");
    }
}

// Add an item to the cart
void addToCart(int productId, int quantity) {
    if (cartCount < MAX_CART_ITEMS) {
        cart[cartCount].product_id = productId;
        cart[cartCount].quantity = quantity;
        cartCount++;
        printf("Item added to the cart!\n");
    } else {
        printf("Unable to add item to the cart. Maximum number of items reached.\n");
    }
}

// List products
void listProducts() {
    printf("Product List:\n");
    for (int i = 0; i < productCount; i++) {
        printf("ID: %d\n", products[i].id);
        printf("Name: %s\n", products[i].name);
        printf("Description: %s\n", products[i].description);
        printf("Price: %.2f\n", products[i].price);
        printf("\n");
    }
}

// View the cart
void viewCart() {
    printf("Shopping Cart:\n");
    for (int i = 0; i < cartCount; i++) {
        int productId = cart[i].product_id;
        int quantity = cart[i].quantity;
        printf("Product ID: %d, Quantity: %d\n", productId, quantity);
    }
}

int main() {
    int choice;

    while (1) {
        printf("Select an option:\n");
        printf("1. Add a product\n");
        printf("2. Add an item to the cart\n");
        printf("3. List products\n");
        printf("4. View the cart\n");
        printf("0. Exit\n");
        scanf("%d", &choice);

        switch (choice) {
            case 1: {
                char name[MAX_NAME_LENGTH];
                char description[MAX_DESCRIPTION_LENGTH];
                float price;
                printf("Enter the product name: ");
                scanf("%s", name);
                printf("Enter the product description: ");
                scanf("%s", description);
                printf("Enter the product price: ");
                scanf("%f", &price);
                addProduct(name, description, price);
                break;
            }
            case 2: {
                int productId, quantity;
                printf("Enter the product ID: ");
                scanf("%d", &productId);
                printf("Enter the quantity: ");
                scanf("%d", &quantity);
                addToCart(productId, quantity);
                break;
            }
            case 3: {
                listProducts();
                break;
            }
            case 4: {
                viewCart();
                break;
            }
            case 0: {
                exit(0);
            }
            default: {
                printf("Invalid choice. Please select another option.\n");
            }
        }
    }

    return 0;
}
