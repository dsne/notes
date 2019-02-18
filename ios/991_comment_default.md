# 기본 주석

## xcode project
- AppDelegate.swift
  - `application, didFinishLaunchingWithOptions`
    - Override point for customization after application launch.
    - 어플리케이션 런처 이후의 커스터마이징을 위한 오버라이딩 위치
  - `applicationWillResignActive`
    - Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state.
    - Use this method to pause ongoing tasks, disable timers, and invalidate graphics rendering callbacks. Games should use this method to pause the game.
  - `applicationDidEnterBackground`
    - Use this method to release shared resources, save user data, invalidate timers, and store enough application state information to restore your application to its current state in case it is terminated later.
    - If your application supports background execution, this method is called instead of applicationWillTerminate: when the user quits.
  - `applicationWillEnterForeground`
    - Called as part of the transition from the background to the active state; here you can undo many of the changes made on entering the background.
  - `applicationDidBecomeActive`
    - Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface.
  - `applicationWillTerminate`
    - Called when the application is about to terminate. Save data if appropriate. See also applicationDidEnterBackground:.
    - 어플리케이션이 종료될 때 호출된다. 적절하게 데이터를 저장하라.
  - 실행 순서
    - 최초 실행: `didFinishLaunchingWithOptions`, `applicationDidBecomeActive`
    - 대기 상태: `applicationWillResignActive`, `applicationDidEnterBackground`
    - 다시 보기: `applicationWillEnterForeground`, `applicationDidBecomeActive`
    - 실행 프로그램 보기 (홈 버튼 더블클릭): `applicationWillResignActive`
    - 실행 프로그램 보기에서 다시 선택: `applicationDidBecomeActive`
    - 실행 프로그램 보기에서 다른 앱 선택: `applicationDidBecomeActive`
    - 실행 프로그램 보기에서 종료: `applicationDidEnterBackground`, `applicationWillTerminate`
