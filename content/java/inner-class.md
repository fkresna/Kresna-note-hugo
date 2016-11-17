+++
title = "Inner Class"
draft = false
date = "2016-11-17T13:41:03+07:00"
tags = ["Java","OCJP"]
categories = ["Programming"]
disqus_url = "note.kresna.xyz"
+++
## Regular Inner Class

    class ClassA{
      private String text = "Some string";
      
      class ClassB{
        public void methodA() {
          System.out.println("MethodA");
        }
      }
    }

## Static Inner Class
    class ClassA1{
      static class ClassB {
        void methodB() {
          System.out.println("methodB");
        }
      }
    }

    class ClassC {
      static class ClassD {
        void methodD() {
          System.out.println("methodD");
        }
      }
      public static void main(String[] args) {
        ClassA1.ClassB ab = new ClassA1.ClassB();
        ab.methodB();

        ClassD classD = new ClassD();
        classD.methodD();
      }
    }

## Method-local Inner Class

## Anonymous Inner Class