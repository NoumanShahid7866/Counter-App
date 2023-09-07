import React , {useState} from 'react';
import {StyleSheet, Text, View, TouchableOpacity} from 'react-native';

const LotsOfStyles = () => {
const [counter, setCounter]= useState(0);
const inc= () => {
setCounter(counter+1);
};
const dec= () => {
setCounter(counter-1);
};
  return (
    <View style={styles.container}>
    <TouchableOpacity onPress={()=> dec()}>
    <View style={styles.btn}>
    <Text  style={styles.txt}> -  </Text>
     </View>
     </TouchableOpacity>
     
     <View style={{width:50, height:50,justifyContent:'center',alignItems:'center',}}>
     <Text style={{fontSize:30}} > {counter} </Text>
     </View>
      <TouchableOpacity onPress={()=> inc()}>
       <View style={styles.btn}>
    <Text style={styles.txt}> + </Text>
     </View>
       </TouchableOpacity>
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex:1 ,justifyContent:'center',alignItems:'center',
    flexDirection:'row',
  },
  bigBlue: {
    color: 'blue',
    fontWeight: 'bold',
    fontSize: 30,
  },
  red: {
    color: 'red',
  },
  btn:{
  backgroundColor:'blue',
  width:50,
  height:50,
  textAlign:'center',
  justifyContent:'center',
  },
  txt:{
  color:'white',
  fontSize:26,
  },
});

export default LotsOfStyles;