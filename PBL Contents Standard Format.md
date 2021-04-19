# PBL Contents Standard Format

![PBL Contents Standard Format_map](https://user-images.githubusercontent.com/47736525/115193729-83163800-a127-11eb-8903-923be6f22a25.png)

## 1. Project

### id
| 형식 | 변수형 | 필수 여부 |
|---|---|----|
| `변수` | `int` | `필수` |

여러 개의 프로젝트를 구분하기 위해 각 프로젝트의 고유 번호를 입력한다.
프로젝트의 고유번호는 4자리 숫자로 구성되며, 서로 다른 프로젝트는 동일한 고유번호를 가질 수 없다. 


### title
| 형식 | 변수형 | 필수 여부 |
|---|---|----|
| `변수` | `string` | `필수` |

프로젝트의 이름을 입력한다. 프로젝트 이름은 한 줄 이내의 핵심적인 내용을 담아, 제목만 보고도 프로젝트를 대략적으로 파악할 수 있도록 한다.

### levels

- `appropriate level` : 프로젝트의 적정 레벨을 'int 변수'로 입력한다. `appropriate level`를 통해 학생들은 해당 프로젝트의 난이도를 가늠할 수 있다.
- `detailed levels` : 프로젝트의 적정 레벨을 'string 배열'로 입력한다. `detailed levels`는 'PSI에서 제공하는 tech-skill 역량명세서 - 수준 구분'을 참고한다.

### objects

- `main object` : 프로젝트의 중추적인 목표를 'string 변수'로 입력한다. `main object`에는 프로젝트가 해결하고자 하는 문제나 프로젝트가 끝났을 때 학생들이 만들어 낼 결과물을 기술한다.
- `detailed objects` : 프로젝트의 세부적인 목표들을 'string 배열'로 입력한다. `main object`를 달성하기 위해 수행할 세부적인 목표들을 기술한다.

### skills

- knowledge skills
- tech skills

	- class
	- experience
	- difficulty

- soft skills

	- class
	- key word
	- action

## 2. Mission

### mission id

### breifing

### kewords

### mission object

- main objects
- detailed objects

	- item
	- optional

### result

### evaluation standard

- item
- class
- tag
- type
- option

### quiz

- class
- question
- answer

## 3. Reference

### answer code link

### data

- file name
- explanation

### resource

- item
- link



*XMind - Trial Version*
