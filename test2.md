#include stdio.h

 

int findMax(int num[],int length){

    int max = -9999999;

    int i,j;

    for(i = 0;i  length;i++){

        int temp = num[i];

        int tempMax = temp;

        for(j = i + 1;j  length;j++){

            if(temp + num[j]  0){

                break;

            }

            temp += num[j];

            if(temp  tempMax){

                tempMax = temp;

            }

        }

        if(tempMax  max){

            max = tempMax;

        }

    }

    return max;

}

 

int main(){

    int d[] = {1, -2, 3, 5, -1};

    int b = findMax(d,5);

    printf(%dn,b);

    int a[] = {1, -2, 3, -8, 5, 1};

    b = findMax(a,6);

    printf(%dn,b);

    int c[] = {1, -2, 3,-2, 5, 1};

    b = findMax(c,6);

    printf(%dn,b);

    return 0;

}

