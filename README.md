# P5 Vector (29. JUNE. 2017  in Modulab)
Vector의 특성에 대해서 알아보고 적용해본 예제입니다.<br>
마우스를 따라 일정한 속도로 움직이는 원을 그립니다.

### Vector의 사전적 의미
벡터(vector)는 크기 만으로 나타낼 수 있는 스칼라(scalar)와 달리 방향과 크기를 사용하여 나타낼 수 있다. 일상적으로 사용하는 벡터는 유향선분(방향이 있는 선분 즉, 화살표)를 써서 표현할 수 있다

### Vector의 특징
#### vector의 표현

>2차원에서의 Vector는 x좌표와 y좌표를 표현할 수 있다.
```
/* Pseudocode */
var vector = { a : 0, b : 0} //x는 x좌표 y는 y좌표
vector.a //실제 x좌표
vector.b //실제 y좌표
```
2차원에서의 Vector는 각도(Radian)와 거리(Distance)를 표현할 수 있다.<br>
```
/* Pseudocode */
var vector = { a : 0, b : 0} //a는 각도(Radian), b는 거리(Distance)
vector.b * cos(vector.a * PI) //실제 x좌표
vector.b * sin(vector.a * PI) //실제 y좌표
```
3차원에서의 Vector는 x, y, z좌표를 표현할 수 있다.<br>
3차원에서의 Vector는 xy평면의 각도, yz평면의 각도, 거리를 표현할 수 있다.<br>

#### vector의 연산
>**normalization(정규화)** : vector를 x좌표와 y좌표로 사용하고 있을때 크기가 1인 Vector로 바꾸고 싶을 때 주로 사용한다.<br>
*주의해야할 점은 normalization을 하면 normal vector가 아니라 unit vector가 된다*
```
/* Pseudocode */
var vector = { x : 0, y : 0 }
var length = sqrt(vector.x * vector.x + vector.y * vector.y)
vector.x / length // Unit Vector의 x
vector.y / length // Unit Vector의 y
```
```
/* Pseudocode */
var vector = { rad : 0, len : 0 }
cos(vector.rad * PI) // Unit Vector의 x
sin(vector.rad * PI) // Unit Vector의 y
```
**dot product(내적 연산)** : 두 백터의 내적 연산은 한 Vector A를 다른 Vector B에 투영시켰을 때의 크기를 계산한다.<br>
**outer product(외적 연산)** : 두 백터의 외적 연산은 두 백터와 모두 수직한 백터 C를 계산한다. 3차원 공간에서 사용된다.<br>

### 실행
네트워크가 되는 환경에서 index.html을 실행합니다.

### 환경
포함되어있는 예제는 P5js를 사용하여 제작되었습니다.

### License

Copyright (c) 2017 Donghyeon Kim (dhygns@naver.com)

Permission is hereby granted, free of charge, to any person obtaining a copy of this
software and associated documentation files (the "Software"), to deal in the Software
without restriction, including without limitation the rights to use, copy, modify, merge,
publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons
to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or
substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE
FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.
