## 1. React Native의 장점(10점)
- React Native를 사용하여 앱을 개발할 때 얻을 수 있는 주요 장점 3가지를 설명하시오.

 

## 2. React Native와 React의 차이점(10점)

- React와 React Native의 주요 차이점을 기술하고, React Native에서 제공하는 고유한 컴포넌트나 기능 3가지를 예를 들어 설명하세요.

 

## 3. 상태 관리(State Management)(10점)

- React Native에서 상태를 관리하기 위한 방법 중 하나로 useState를 사용하여 버튼을 누르면 숫자가 1씩 증가하는 카운터 예제를 만드세요

 

## 4. 스타일링(Styling)(10점)

- React Native에서 StyleSheet를 사용하여 스타일을 정의하는 방법을 설명하고, 동적으로 스타일을 적용해야 하는 상황에서 어떻게 처리할 수 있는지 코드와 함께 설명하세요.
 

## 5. 네비게이션(Navigation)(10점)

- React Native에서 네비게이션의 패턴 3가지와 각각의 개념에 대해 설명하세요.

 
## 6. 플랫폼별 차이 처리(10점)

- React Native에서 iOS와 Android를 구별하여 관리하는 Platform API에서 OS와 버전을 구분하는 키워드를 각각 쓰세요.
 

## 7. React Native에서 Context API를 사용하여 테마(다크 모드/라이트 모드)를 전역으로 관리하는 코드를 작성하세요.(20점)

 

### 요구사항
```
Context 생성: 테마를 관리하기 위한 Context를 생성하세요.
Provider 구현: 테마 상태를 관리하고 하위 컴포넌트에 테마 데이터를 제공하는 Provider 컴포넌트를 구현하세요.
테마는 두 가지 값(라이트 모드와 다크 모드) 중 하나여야 합니다.
버튼을 눌러 테마를 토글할 수 있어야 합니다.
테마 적용: 텍스트를 가지는 ThemeComponent, 버튼을 가지는 ThemeToggleButton 두 개의 하위 컴포넌트에서 전역 테마 데이터를 읽어 각기 다른 스타일을 적용하세요.
```
------------------------------------------------------------------------
```
제공 스타일

// 라이트 테마 스타일
const lightThemeStyles = StyleSheet.create({
 container: {
   flex: 1,
   justifyContent: 'center',
   alignItems: 'center',
 },
 box: {
   backgroundColor: '#fff',
   padding: 20,
   borderRadius: 8,
 },
 text: {
   color: '#000',
   fontSize: 18,
 },
});

// 다크 테마 스타일
const darkThemeStyles = StyleSheet.create({
 container: {
   flex: 1,
   justifyContent: 'center',
   alignItems: 'center',
 },
 box: {
   backgroundColor: '#333',
   padding: 20,
   borderRadius: 8,
 },
 text: {
   color: '#fff',
   fontSize: 18,
 },
});
```
------------------------------------------------------------------------

 

## 8. React Navigation을 사용하여 스택 네비게이션과 바텀 탭 네비게이션을 함께 구현하는 코드를 작성하세요.(20점)
```
요구사항

필요한 라이브러리 설치하기

- react-navigation/bottom-tabs": 6.5.20,
- react-navigation/native: 6.1.18,

- react-navigation/stack: 6.4.1,

- react-native-gesture-handler
- react-native-reanimated
- react-native-screens
- react-native-community/masked-view
- react-native-safe-area-context
 
바텀 탭 네비게이션 구현

- 두 개의 스크린(Home, Profile)을 포함하세요.
- 각 탭에는 텍스트로 탭 이름이 표시됩니다.
- Home은 눌렸을 때는 home, 안누렸을 때는 home-outline으로 표시
- Profile은 눌렸을 때는 account, 안눌렸을 때는 account-outline으로 표시
- Home화면은 Home Screen이라는 텍스트와 ‘Details’로 넘어가는 버튼이 있다.
- Profile화면은 Profile Screen이라는 텍스트를 가지고 있다.
 
스택 네비게이션 구현

- 바텀 탭 네비게이션을 포함하는 화면을 Tabs라는 이름으로 설정하세요.
- Tab네비게이션에서는 스택의 헤더를 숨겨주세요.
- 스택 네비게이션에는 Details라는 추가 화면이 포함되어야 합니다.
- Details는 Details Screen이라는 텍스트만 갖는다.
- Home 탭에서 버튼을 클릭하면 Details 화면으로 이동할 수 있어야 합니다.
 
탭바 동작

Home과 Profile 화면에서는 탭바가 보여야 합니다.
Details 화면에서는 탭바가 보이지 않아야 합니다.
```
### 해답

```js
import React from 'react';
import { View, Text, Button } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import { createStackNavigator } from '@react-navigation/stack';
import Ionicons from 'react-native-vector-icons/Ionicons';

// 바텀 탭 네비게이션
const Tab = createBottomTabNavigator();

const HomeScreen = ({ navigation }) => (
  <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
    <Text>Home Screen</Text>
    <Button
      title="Go to Details"
      onPress={() => navigation.navigate('Details')}
    />
  </View>
);

const ProfileScreen = () => (
  <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
    <Text>Profile Screen</Text>
  </View>
);

const Tabs = () => (
  <Tab.Navigator
    screenOptions={({ route }) => ({
      tabBarIcon: ({ focused, color, size }) => {
        let iconName;

        if (route.name === 'Home') {
          iconName = focused ? 'home' : 'home-outline';
        } else if (route.name === 'Profile') {
          iconName = focused ? 'person' : 'person-outline';
        }

        return <Ionicons name={iconName} size={size} color={color} />;
      },
      tabBarActiveTintColor: 'tomato',
      tabBarInactiveTintColor: 'gray',
    })}
  >
    <Tab.Screen name="Home" component={HomeScreen} />
    <Tab.Screen name="Profile" component={ProfileScreen} />
  </Tab.Navigator>
);

// 스택 네비게이션
const Stack = createStackNavigator();

const DetailsScreen = () => (
  <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
    <Text>Details Screen</Text>
  </View>
);

const App = () => (
  <NavigationContainer>
    <Stack.Navigator>
      {/* Tabs를 스택 네비게이션의 첫 화면으로 설정 */}
      <Stack.Screen
        name="Tabs"
        component={Tabs}
        options={{ headerShown: false }} // Tabs에서는 헤더를 숨김
      />
      {/* Details 화면 추가 */}
      <Stack.Screen name="Details" component={DetailsScreen} />
    </Stack.Navigator>
  </NavigationContainer>
);

export default App;
```

