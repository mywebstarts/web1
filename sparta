# 하림님 팔
from Robot_Arms import arm_act, arm_check
# 유림님 다리
from Robot_Legs import leg_act, leg_check
# 지호님 장비
from Robot_Weapons import weapon_act, weapon_check
# 명혜님 머리
from Robot_Head import head_act, head_check


def start(engine_start):
    # engine_start가 "On"일 때 시동을 켬
    if engine_start.lower() == "on":
        print("시동을 켰습니다.")
        print()
        head_check(engine_start)
        print()
        arm_check(engine_start)
        print()
        leg_check(engine_start)
        print()
        weapon_check(engine_start)
        print()
        operation_choice()

    elif engine_start.lower() == "off":
        print("시동을 키지 않겠습니다. 시스템을 종료합니다")
    else:
        print("올바른 값을 입력해주세요. ('Off' 또는 '0n')")

    return engine_start


def operation_choice():
    while True:
        print("어떤 행동을 하시겠습니까?")
        print()
        print("1. 움직인다")
        print("2. 팔을 움직인다")
        print("3. 무기를 사용한다")
        print("4. 시야를 체크한다")
        choice = input("어떤 행동을 할지 숫자로 입력해주세요: ")
        operate_function(choice)
        repeat = input("다시 행동 하시겠습니까? (yes or other) : ")

        if repeat.lower() == "yes" :
            print()
            print("재시작 하겠습니다!")
            print()
        else : 
            print()
            print("시스템을 종료합니다!")
            print()
            break
        


def operate_function(choice):
    if choice == "1":
        right_leg = int(input('점프를 시도해볼까요? (0부터 10까지 입력)'))
        left_leg = int(input('점프를 시도해볼까요?(0부터 10까지 입력)'))
        print(leg_act(right_leg, left_leg))

    elif choice == "2":
        arm_grab = input("어떤 손 동작을 실행 시킬까요? (1 or 2)")
        arm_act(arm_grab)
    elif choice == "3":
        weapon_act()
    elif choice == "4":
        print("머리의 작동은 동시에 진행됩니다! 스캔 과 발성 기능의 실행여부를 입력해 주세요.")
        operate_eye = int(input("스캔 기능을 실행 시키겠습니까? (0 or 1) : "))
        operate_mouth = int(input("발성 기능을 실행 시키겠습니까? (0 or 1) : "))
        print(head_act(operate_eye, operate_mouth))
    else:
        print("명령을 알아들을수 없습니다.")


# 사용자 입력을 받음
engine_start = input("로봇의 시동을 거시려면 on을 입력하십시오. (on/off)")

# start 함수 호출 및 결과 출력
start(engine_start)
