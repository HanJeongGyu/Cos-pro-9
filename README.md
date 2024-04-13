# Cos-pro-9

```c
#include <stdio.h>

// 함수 선언
void example1(void); // 예제 함수 1 선언
void example2(void); // 예제 함수 2 선언
void example3(void); // 예제 함수 3 선언
int GetAbsoValue(int num); // 절대값을 반환하는 함수 선언
int AbsoCompare(int num1, int num2); // 두 정수 중 절대값이 큰 값을 반환하는 함수 선언
int add(int num1, int num2); // 두 정수를 더하는 함수 선언
int sub(int num1, int num2); // 두 정수를 빼는 함수 선언
void ShowAddResult(int num); // 덧셈 결과를 출력하는 함수 선언
int ReadNum(void); // 사용자로부터 정수를 입력받는 함수 선언
void HowToUseThisProg(void); // 프로그램 사용 방법을 출력하는 함수 선언

int main(void)
{
    int num1, num2;
    
    printf("두 정수를 입력하세요:\n");
    scanf_s("%d %d", &num1, &num2); // 사용자로부터 두 정수를 입력받음
    
    printf("%d와 %d 중 절대값이 큰 정수는: %d\n", num1, num2, AbsoCompare(num1, num2)); // 입력된 두 정수 중 절대값이 큰 정수를 출력
    
    // 예제 함수를 테스트하려면 주석을 해제합니다.
    // example1();
    // example2();
    // example3();
    
    return 0;
}

// 함수 정의

// 절대값을 반환하는 함수 정의
int GetAbsoValue(int num)
{
    if (num < 0)
    {
        return num * (-1);
    }
    else
    {
        return num;
    }
}

// 두 정수 중 절대값이 큰 값을 반환하는 함수 정의
int AbsoCompare(int num1, int num2)
{
    if (GetAbsoValue(num1) > GetAbsoValue(num2))
    {
        return num1;
    }
    else
    {
        return num2;
    }
}

// 두 정수를 더하는 함수 정의
int add(int num1, int num2)
{
    return num1 + num2;
}

// 두 정수를 빼는 함수 정의
int sub(int num1, int num2)
{
    return num1 - num2;
}

// 덧셈 결과를 출력하는 함수 정의
void ShowAddResult(int num)
{
    printf("덧셈 결과: %d\n", num);
}

// 사용자로부터 정수를 입력받는 함수 정의
int ReadNum(void)
{
    int num;
    scanf_s("%d", &num);
    return num;
}

// 프로그램 사용 방법을 출력하는 함수 정의
void HowToUseThisProg(void)
{
    printf("이 프로그램은 두 정수를 입력받아 합을 출력합니다.\n");
    printf("두 정수를 입력하세요:\n");
}

// 예제 함수 1 정의
void example1(void)
{
    int num1 = 0;
    
    // printf 함수는 출력된 문자 수를 반환합니다.
    num1 = printf("1234\n");
    printf("    num : %d\n", num1);
}

// 예제 함수 2 정의
void example2(void)
{
    int test = 0;
    
    // add 함수 테스트
    test = add(1, 2);
    printf("add test = %d \n", test);
    ShowAddResult(test);
    
    // sub 함수 테스트
    test = sub(1, 2);
    printf("sub test = %d \n", test);
}

// 예제 함수 3 정의
void example3(void)
{
    int num1 = 0, num2 = 0, test = 0;
    
    HowToUseThisProg(); // 프로그램 사용 방법 출력
    
    num1 = ReadNum(); // 첫 번째 정수 입력
    num2 = ReadNum(); // 두 번째 정수 입력
    
    test = add(num1, num2); // 입력된 두 정수를 더함
    ShowAddResult(test); // 덧셈 결과 출력
}
```
