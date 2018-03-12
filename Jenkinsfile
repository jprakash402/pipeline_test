#!groovy
import groovy.json.JsonSlurperClassic
/*
This is a test file to checkout scm and echo variables
*/
pipiline {
 agent any
  stage ('SCM Checkout')
   {
     steps 
     {
      checkout scm
      //def props = readJSON file: './repo.json'
      def key_values = new JsonSlurper().parse(new File('./repo.json'))
      //def key_vaues = readJSON file: './json.json'
      def test_key = key_values.version
      echo '${test_key}'
      }
   }
}
