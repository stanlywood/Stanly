# Stanly
repository
package com.ecnu.extendsdemo;

class People{
	private int age;
	//子类不能访问父类的私有成员

	public int getAge() {
		return age;
	}

	public void setAge(int age) {
		this.age = age;
	}
}

class Worker extends People{	//类名首字母大写
	
}

class Petworker extends Worker{		//单继承，没有哪个类继承两次
		void tell(){
			System.out.println(getAge());
		}							//一个孩子只能有一个亲生父亲
									//可以多层继承
}

public class ExtendsDemo02 {

	public static void main(String[] args) {
		Petworker zhangsan  = new Petworker(); 
		zhangsan.setAge(100);
		zhangsan.tell();
	}

}
