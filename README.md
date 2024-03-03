#include<stdio.h>
#include<graphics.h>
#include<conio.h>
void pixel(int xc,int yc,int x,int y);
void main()
{
int gd=DETECT,gm,xc,yc,x,y,r,pk;
clrscr();
initgraph(&gd,&gm,"c:\\turboc3\\bgi");
printf("***mid point circle algo***\n");
printf("enter the value of xc:");
scanf("%d",&xc);
printf("enter the value of yc:");
scanf("%d",&yc);
printf("enter the redius :");
scanf("%d",&r);
x=0;
y=r;
pk=1-r;
pixel(xc,yc,x,y);
whlie(x<y)
{
if(pk<0)
{
x=x+1;
pk=pk+(2*x)+1;
}
else
{
x=x+1;
y=y-1;
pk=pk+(2*x)-(2*y)+1;
}
pixel(xc,yc,x,y);
}
getch();
closegraph();
}
void pixel(int xc,int yc,int x,int y)
{
putpixel(xc+x,yc+y,7);
putpixel(xc+y,yc+x,7);
putpixel(xc-y,yc+x,7);
putpixel(xc-x,yc+y,7);
putpixel(xc-x,yc-y,7);
putpixel(xc-y,yc-x,7);
putpixel(xc+y,yc-x,7);
putpixel(xc+x,yc-y,7);
}

