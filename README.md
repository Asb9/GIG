npm install @react-navigation/drawer
import { NavigationContainer } from '@react-navigation/native';

// In your App component
return (
  <NavigationContainer>
    {/* Rest of your navigation setup */}
  </NavigationContainer>
);
import React from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';
import { DrawerItemList } from '@react-navigation/drawer';

const CustomDrawerContent = (props) => {
  return (
    <View style={{ flex: 1 }}>
      {/* Header */}
      <View style={styles.drawerHeader}>
        <Text style={styles.headerText}>My Custom Header</Text>
      </View>

      {/* Drawer Items */}
      <DrawerItemList {...props} />

      {/* Footer */}
      <View style={styles.drawerFooter}>
        <Button title="Custom Button 1" onPress={() => {/* handle action */}} />
        <Button title="Custom Button 2" onPress={() => {/* handle action */}} />
      </View>
    </View>
  );
};

const styles = StyleSheet.create({
  drawerHeader: {
    // Your styling for the header
  },
  headerText: {
    // Your styling for the header text
  },
  drawerFooter: {
    // Your styling for the footer
    marginTop: 'auto' // Pushes the footer to the bottom
  }
});

export default CustomDrawerContent;h
import { createDrawerNavigator } from '@react-navigation/drawer';
import CustomDrawerContent from './path-to/CustomDrawerContent';

const Drawer = createDrawerNavigator();

function MyDrawer() {
  return (
    <Drawer.Navigator drawerContent={(props) => <CustomDrawerContent {...props} />}>
      {/* Your Drawer Screens */}
    </Drawer.Navigator>
  );
}
