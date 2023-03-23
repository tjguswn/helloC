# 4주차 c언어 실습

#include <stdio.h>
#define _CRT_SECURE_NO_WARNINGS
#define SEC_PER_MINUTE 60

int main(void)
{
    int money, change;
    int price, p1000, p500, p100;
    
    printf("물건 값을 입력하시오: ");
    scanf("%d", &price);
    printf("투입한 금액을 입력하시오: ");
    scanf("%d", &money);
    printf("거스름돈은 다음과 같습니다.\n\n");

    change = money - price;

    p1000 = change / 1000;
    change = change % 1000;

    p500 = change / 500;
    change = change % 500;

    p100 = change / 100;

    printf("천원권: %d장\n", p1000);
    printf("오백원 동전: %d개\n", p500);
    printf("백원 동전: %d개\n", p100);

    return 0;
}
