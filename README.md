EXP 1. Implement linear and binary search algorithms, then analyze and evaluate their time complexity

      LINEAR SEARCH
      
      #include<stdio.h>
      void main()
      {
        int a[20], i, n, key, flag = 0, pos;
        printf("Enter values of n : ");
        scanf("%d", &n);
        //Code to read array of elements
        for(i=0;i<n;i++){
          printf("Enter elements for a[%d] : ",i);
          scanf("%d",&a[i]);
        }
          printf("Enter key elements : ");
          scanf("%d", &key);
        //Code for linear search process
        for(i=0;i<n;i++){
          if(a[i]==key)
          {
            flag=1;
            pos=i;
            break;
          }
        }
        if(flag==1){
          printf("The key element %d is found at the position %d\n", key, pos);
      } else {
          printf("The key element %d is not found in the array\n", key);
      }
      }


      BINARY SEARCH

      #include<stdio.h>
      void main()
      {
        int a[20], i, j, n, key, flag=0, low, high, mid, temp;
        printf("Enter value of n  : ");
        scanf("%d",&n);
        //Code to read an array of elements
              for(i=0;i<n;i++){
                printf("Enter elements for a[%d] : ", i);
                scanf("%d",&a[i]);
              }
              for(i=0;i<n-1;i++){
                for(j=0;j<n-1;j++){
                  if(a[j]>a[j+1]){
                    temp=a[j];
                    a[j]=a[j+1];
                    a[j+1]=temp;
                  }
                }
              }
              printf("Enter key elements : ");
              scanf("%d", &key);
        //Code to sort the elements using any sorting technique
              printf("After sorting the elements in the array are\n");
              for(i=0;i<n;i++){
                   printf("Value of a[%d] = %d\n", i, a[i]);
              }
              low=0;
              high=n-1;
              while(low<=high){
                      mid=(low+high)/2;
                      if(a[mid]==key){
                            flag=1;
                            break;
                      } else if (a[mid] < key){
                            low=mid+1;
                      } else {
                            high = mid - 1;
                      }
              }
            if(flag == 1){
                  printf("The key element %d is found at the position %d\n", key, mid);
            } else {
                        printf("The key element %d is not found in the array\n", key);
            }
      }



EXP 2. Implement Bubble, Selection, and Insertion sort algorithms, and analyze their time complexity

      SELECTION SORT

      #include<stdio.h>
      void main()
      {
            int a[20], i, n, j, large, index;
            printf("Enter value of n : ");
            scanf("%d", &n);
            //Code to read an array elements
            for(i=0; i<n; i++){
                  printf("Enter elements of a[%d] : ", i);
                  scanf("%d", &a[i]);
            }
            printf("Before sorting the elements in the array are\n");
            //Code to print the given array elements before sorting
            for(i=0; i<n; i++){
                  printf("Value of a[%d] = %d\n", i, a[i]);
            }
            //Code for selection sort largest element method
            for(i=n-1; i>0; i--){
                  large = a[0];
                  index = 0;

            for(j=1; j<=i; j++){
                  if(a[j]>large){
                        large = a[j];
                        index = j;
                  }
            }
            int temp = a[i];
            a[i] = a[index];
            a[index] = temp;
            }
            printf("After sorting the elements in the array are\n");
            //Code to print the given array element after sorting
            for(i=0; i<n; i++){
                  printf("Value of a[%d] = %d\n", i, a[i]);
            }
      }


      BUBBLE SORT

      #include<stdio.h>
      #include<strin.h>
      void main()
      {
            char a[20][20];
            int i, n, j;
            char temp[20];
            printf("Enter value of n : ");
            scanf("%d", &n);
            //Code to read n strings.
            for(i=0; i<n; i++){
                  printf("Enter string for a[%d] : ",i);
                  scanf("%s", a[i]);
            }
            printf("Before sorting the string in the array are\n);
            //Code to print the string before sorting
            for(i=0; i<n; i++){
                  printf("String at a[%d] = %s\n", i, a[i]);
                  }
            //Code to sort the strings using bubble sort technique
            for(i=0; i<n-1; i++){
                  for(j=0; j<n--i-1; j++){
                        if(strcmp(a[j],a[j+1])>0){
                              strcpy(temp,a[j]);
                              strcpy(a[j],a[j+1]);
                              strcpy(a[j+1],temp);
                        }
                  }
            }
            printf("After sorting the strings in the array are\n");
            //Code to print the string after sorting
            for(i=0; i<n; i++){
                  printf("String at a[%d] = %s\n", i, a[i]);
            }
      }
      
            
            
      
