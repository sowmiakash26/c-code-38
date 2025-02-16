#include <stdio.h>
#include <stdlib.h>
int main() {
    int *arr,n,new;
    printf("Enter n number of elements:");
    scanf("%d",&n);
    arr = (int *)malloc(n *sizeof(int));
    
    if(arr==NULL){
        printf("Memory allocation failed\n");
        return 1;
    }
    printf("Enter %d elements:\n",n);
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    printf("Entered elements are:\n");
    for(int i=0;i<n;i++){
        printf("%d ",arr[i]);
    }
    printf("\n");
    printf("Enter the new size of array:");
    scanf("%d",&new);
    arr = (int *)realloc(arr,new * sizeof(int));
    if(arr==NULL){
        printf("Memory allocation is failed \n");
        return 1;
    }
    printf("Enter %d elements: \n",n);
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    printf("Entered elements are:\n");
    for(int i=0;i<n;i++){
        printf("%d ",arr[i]);
    }
    printf("\n");
    free(arr);
    return 0;
    
}
