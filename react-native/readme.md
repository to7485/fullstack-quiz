## 1. React Native의 장점(10점)
- React Native를 사용하여 앱을 개발할 때 얻을 수 있는 주요 장점 3가지를 설명하시오.

### 해답
```
크로스 플랫폼 개발:
React Native는 하나의 코드베이스로 iOS와 Android 앱을 동시에 개발할 수 있어 개발 시간이 단축되고 유지보수가 쉬워집니다. 예를 들어, StyleSheet를 활용해 플랫폼 간 공통 UI를 정의할 수 있습니다.

핫 리로드:
코드를 저장하면 앱이 즉시 새로고침되며 변경 사항을 반영합니다. 이는 개발 생산성을 크게 높여줍니다. 예를 들어, UI 컴포넌트의 색상을 변경한 후 저장하면 즉시 결과를 확인할 수 있습니다.

React 생태계 활용:
JavaScript와 React의 강력한 생태계를 활용할 수 있어 수많은 라이브러리와 툴을 사용할 수 있습니다. 예를 들어, 상태 관리에 Redux를 사용할 수 있습니다.
```
 

## 2. React Native와 React의 차이점(10점)

- React와 React Native의 주요 차이점을 기술하고, React Native에서 제공하는 고유한 컴포넌트나 기능 3가지를 예를 들어 설명하세요.

### 해답
```
정답:
React는 웹 애플리케이션 개발에 특화되어 있고, React Native는 모바일 애플리케이션 개발을 위해 만들어졌습니다.
React Native의 고유한 컴포넌트와 기능:

View:
웹의 div와 유사하지만, 모바일 환경에 최적화된 레이아웃 컴포넌트입니다.
Text:
웹의 p와 비슷하며, 텍스트를 렌더링할 때 사용됩니다.
StyleSheet:
CSS와 유사하지만, JavaScript 객체로 스타일을 정의합니다.
```

## 3. 상태 관리(State Management)(10점)

- React Native에서 상태를 관리하기 위한 방법 중 하나로 useState를 사용하여 버튼을 누르면 숫자가 1씩 증가하는 카운터 예제를 만드세요

 

## 4. React Native에서 StyleSheet의 개념과 특징을 설명하시오(10점)
### 해답
```
1. StyleSheet의 개념
StyleSheet는 React Native에서 UI를 스타일링하기 위해 사용하는 API입니다. JavaScript 객체 형태로 스타일을 정의하며, 이를 통해 React Native 컴포넌트에 적용할 수 있습니다.

2. StyleSheet의 주요 특징

JavaScript 기반 스타일링:

스타일을 JavaScript 코드로 작성하여 동적으로 설정할 수 있습니다.
스타일 객체를 변수처럼 저장하거나, 조건에 따라 스타일을 변경할 수 있습니다.

CSS-like 문법:

CSS와 비슷한 속성을 사용하므로 웹 개발자들이 쉽게 배울 수 있습니다.
예: backgroundColor, fontSize, margin 등.
```
 

## 5.  React Native에서 네비게이션의 패턴 3가지와 각각의 개념에 대해 설명하세요.(10점)
1. Stack Navigation
```
개념:
Stack Navigation은 화면들을 스택(Stack)처럼 쌓아 관리하며, 새로운 화면이 열리면 기존 화면 위에 쌓이고, 뒤로가기 버튼을 통해 이전 화면으로 이동할 수 있습니다.
특징:
기본적인 네비게이션 패턴으로 화면 전환 애니메이션이 포함됩니다.
사용자가 뒤로가기를 통해 이전 화면으로 쉽게 돌아갈 수 있습니다.
사용 사례:
로그인 화면 → 메인 화면 → 상세 화면 같은 단계적인 화면 흐름을 구현할 때 유용합니다.
```
2. Bottom Tab Navigation
```
개념:
화면 하단에 탭 바(Tab Bar)를 표시하여 사용자가 탭을 눌러 화면 간에 이동할 수 있도록 합니다.
특징:
탭 간 이동 시 화면의 상태를 유지합니다.
직관적인 UI를 제공하여 사용자가 주요 화면에 쉽게 접근할 수 있습니다.
사용 사례:
소셜 미디어 앱에서 홈, 프로필, 설정 같은 주요 기능을 제공하는 경우.
```
3. Drawer Navigation
```
개념:
화면의 왼쪽(또는 오른쪽)에 숨겨진 메뉴를 드로어(Drawer) 형태로 표시하며, 메뉴를 열어 다른 화면으로 이동할 수 있습니다.
특징:
화면 공간을 절약하면서도 다양한 화면으로 이동할 수 있는 옵션을 제공합니다.
드로어는 제스처나 버튼 클릭으로 열리고 닫힙니다.
사용 사례:
이메일 앱처럼 메뉴 옵션이 많을 때, 드로어를 통해 폴더 또는 설정 화면으로 이동할 수 있습니다.
```
 
## 6. React Native에서 iOS와 Android를 구별하여 관리하는 Platform API에서 OS와 버전을 구분하는 키워드를 각각 쓰세요.(10점)
- OS를 구분하기 위한 키워드: Platform.OS
- OS 버전을 확인하기 위한 키워드: Platform.Version
 

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

### 해답
```
import React, { createContext, useState, useContext } from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';

// 1. Context 생성
const ThemeContext = createContext();

// 2. Provider 구현
const ThemeProvider = ({ children }) => {
  const [isDarkMode, setIsDarkMode] = useState(false);

  const toggleTheme = () => setIsDarkMode(!isDarkMode);

  const theme = {
    isDarkMode,
    toggleTheme,
    styles: isDarkMode
      ? darkThemeStyles
      : lightThemeStyles,
  };

  return (
    <ThemeContext.Provider value={theme}>
      {children}
    </ThemeContext.Provider>
  );
};

// 3. 하위 컴포넌트에서 테마 적용
const ThemedComponent = () => {
  const { styles } = useContext(ThemeContext);
  return (
    <View style={[styles.container, styles.box]}>
      <Text style={styles.text}>This is a themed box!</Text>
    </View>
  );
};

const ThemeToggleButton = () => {
  const { toggleTheme, isDarkMode } = useContext(ThemeContext);
  return (
    <Button
      title={isDarkMode ? 'Switch to Light Mode' : 'Switch to Dark Mode'}
      onPress={toggleTheme}
    />
  );
};

// 4. 메인 앱 구성
const App = () => {
  return (
    <ThemeProvider>
      <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
        <ThemedComponent />
        <ThemeToggleButton />
      </View>
    </ThemeProvider>
  );
};

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

export default App;
```

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

