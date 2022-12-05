# ```git add [filename]```  

- WD의 변경사항을 SA로 이동
- 모든 파일을 add하기   
```git add .```  

# ```git commit [filename]```  
- SA의 내용을 Repository로 이동
- ```-m [message]``` 커밋 메세지 입력
- ```-a``` Staged 되지 않은 변경사항을 commit함

# ```git log```
- commit 기록을 표시
- ```--oneline``` 한 줄에 표시
- ```--all``` 다른 branch의 commit도 표시
- ```--graph``` commit 간의 연결을 그래프로 표시

# ```git show [hash]```
- commit의 자세한 정보를 표시, 기본값은 가장 최근 커밋
- commit의 hash나 HEAD, HEAD~2와 같이 commit을 지정할 수 있음

# ```git clone [repository] [name]```
- 저장소를 복사하는 명령어
- name에 저장소 이름을 지정할 수 있음

# ```push, pull```
- ```git push``` Local Repository의 변경사항을 내보내기
- ```git pull``` Remote Repository의 변경사항을 받아오기

# ```git branch```
- branch 관련 명령어
- ```--list``` branch 목록을 표시
- ```-d [branch] ``` branch 삭제
- ```-m [branch] [newbranch] ``` branch 이름 변경
# ```git merge [branch]```
- 현재 작업중인 branch에, 입력한 branch를 병합

## Fast-Forward merge
![image](https://user-images.githubusercontent.com/112846041/205550022-ba7cb457-e966-458f-8555-343b758f3135.png)
- branch가 일렬로 나열되어 있을 때, 병합은 HEAD를 변경하는 것으로 완료
- 이 경우에도 ```--no-ff``` 옵션으로 3-way merge를 할 수 있음

## 3-way merge
![image](https://user-images.githubusercontent.com/112846041/205550722-0f9e2975-30e8-467d-9de1-748cdb1fed0b.png)
- branch가 분기되어 있을 때, 두 branch를 병합할 경우 Conflict의 가능성이 있음
- Conflict가 발생한 경우. 내용 수정 후 commit하여 병합 완료

## ```rebase```
![image](https://user-images.githubusercontent.com/112846041/205552331-7e5b3c3d-b2da-4146-b264-9f64871f3ae0.png)

- 분기된 branch를 앞쪽에 재배치하는 것
- feature branch에서 ```git rebase main```을 입력해, feature branch를 main branch의 HEAD 뒤에 배치함
- 이후 main branch에서 Fast-Forward merge 하여 병합 완료

