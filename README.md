# OpenGL-Program-that-Draws-the-first-letters-of-you-first-and-last-name
//Created by: Kian Rey Sagala

#include <GL/glut.h>
		
		void display();
		void reshape(int,int);
		void timer(int);
		
		void init()
		{
		glClearColor(0.0f, 0.0f, 0.0f, 0.0f);
		glEnable(GL_DEPTH_TEST);
		
		}
		
		int main(int argc,char**argv)
		{
		glutInit(&argc,argv);
		glutInitDisplayMode(GLUT_RGB | GLUT_DOUBLE | GLUT_DEPTH);
		glutInitDisplayMode(GLUT_RGB);
		
		glutInitWindowPosition(0,0);
		glutInitWindowSize(800,700);
		glutCreateWindow("KS");
		
		
		glutDisplayFunc(display);
		glutReshapeFunc(reshape);
		glutTimerFunc(0,timer,0);
		init();
		
		glutMainLoop();
		}
		
		
		void display()
		{
		
		
		glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);
		glLoadIdentity();

			
		glTranslatef(0.0f,0.0f,-8.0);
		
		glBegin(GL_QUADS);
	//K Base!
	glColor3f(1.0,0.0,0.0);
	glVertex2f(-1.0,0.0);
	glVertex2f(-1.0,-10.0);
	glVertex2f(0.0,-10.0);
	glVertex2f(0.0,0.0);
	//K Upper slant Line!
	glColor3f(1.0,1.0,0.0);
	glVertex2f(3.0,0.0);
	glVertex2f(0.0,-4.0);
	glVertex2f(0.0,-5.0);
	glVertex2f(5.0,0.0);

	//K lower slant line!
	glColor3f(1.0,1.0,0.0);
	glVertex2f(0.0,-5.0);
	glVertex2f(3.0,-10.0);
	glVertex2f(5.0,-10.0);
	glVertex2f(0.0,-4.0);

	//1st
	glColor3f(1.0,1.0,0.0);
	glVertex2f(7.0,-5.0);
	glVertex2f(7.0,-7.0);
	glVertex2f(8.25,-7.5);
	glVertex2f(8.15,-5.0);
	//2nd
	glColor3f(1.0,0.0,0.0);
	glVertex2f(7.0,-7.0);
	glVertex2f(7.25,-9.0);
	glVertex2f(7.75,-9.5);
	glVertex2f(8.25,-7.5);
	//3rd
	glColor3f(1.0,0.0,0.0);
	glVertex2f(7.75,-9.5);
	glVertex2f(9.25,-10.0);
	glVertex2f(9.15,-8.0);
	glVertex2f(8.25,-7.5);
	//4th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(9.15,-8.0);
	glVertex2f(9.25,-10.0);
	glVertex2f(9.0,-8.0);
	glVertex2f(10.80,-8.0);
	//5th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(10.0,-7.0);
	glVertex2f(9.20,-8.0);
	glVertex2f(10.80,-8.0);
	glVertex2f(11.0,-7.0);
	//6th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(9.0,-6.0);
	glVertex2f(9.80,-7.0);
	glVertex2f(11.0,-7.0);
	glVertex2f(10.75,-6.0);
	//7th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(8.5,-5.0);
	glVertex2f(9.0,-6.0);
	glVertex2f(10.75,-6.0);
	glVertex2f(10.0,-5.0);
	//8th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(8.25,-4.0);
	glVertex2f(8.5,-5.0);
	glVertex2f(10.0,-5.0);
	glVertex2f(9.25,-4.0);
	//9th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(8.0,-2.5);
	glVertex2f(8.25,-4.0);
	glVertex2f(9.25,-4.0);
	glVertex2f(8.75,-2.5);
	//10th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(8.5,-0.5);
	glVertex2f(8.0,-2.5);
	glVertex2f(8.75,-2.5);
	glVertex2f(9.0,-2.0);
	//11th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(8.5,-0.5);
	glVertex2f(8.0,-2.5);
	glVertex2f(9.5,-2.0);
	glVertex2f(9.5,-0.0);
	//12th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(9.5,-0.0);
	glVertex2f(9.5,-2.0);
	glVertex2f(10.0,-2.0);
	glVertex2f(10.0,-0.25);
	//13th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(10,-0.25);
	glVertex2f(10.0,-2.0);
	glVertex2f(10.5,-2.5);
	glVertex2f(10.75,-1.0);
	//14th
	glColor3f(1.0,0.0,0.0);
	glVertex2f(10.75,-1.0);
	glVertex2f(10.5,-2.5);
	glVertex2f(10.5,-2.5);
	glVertex2f(11.5,-2.75);
	//15th
	glColor3f(1.0,1.0,0.0);
	glVertex2f(10.5,-2.5);
	glVertex2f(10.5,-5.0);
	glVertex2f(11.5,-5.0);
	glVertex2f(11.5, -2.75);


	glEnd();

	glutSwapBuffers();
}
		
		void reshape(int w, int h)
		{
		glViewport(0,0, (GLsizei)w, (GLsizei)h);
		glMatrixMode(GL_PROJECTION);
		glLoadIdentity();
		gluPerspective(150,1,2.0,100.0);
		glMatrixMode(GL_MODELVIEW);
		
		}
		
		void timer(int)
		{
		glutPostRedisplay();
		glutTimerFunc(1000/60,timer,0);
		
		}
