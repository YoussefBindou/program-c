#include<stdio.h>
 int main (){
		int tabl[50],tpos[50],tneg[50];
		int i,somme,max,min,pmax,pmin,nbre;
		int rang,j,p,k,l,g;

		
		somme=0;
		for(i=0;i<50;i++){
		printf("donne nombre %d:",i+1);
		scanf ("%d",&tabl[i]);
		}
		//affichaj
		for(i=0;i<50;i++){
		printf("%d\n",tabl[i]);
		}
		
		//la somme
		for(i=0;i<50;i++){
		somme=somme+tabl[i];
		}
		printf("somme est :%d\n",somme);
		
		//afiche la max et min
		max=tabl[0];
		min=tabl[0];
		pmax=0;
		pmin=0;
		for(i=1;i<50;i++){
			if(tabl[i]>max){
				max=tabl[i];
				pmax=i;
			} 
			if(tabl[i]<min){
				min=tabl[i];
				pmin=i;
			}
		}
		printf("max est : %d position est : %d\n",max,pmax);
		printf("min est : %d position est : %d\n",min,pmin);
		
		//ranger la tabl
		for(i=0;i<50;i++){
			for(j=i;j<50;j++){
				if(tabl[i]>tabl[j]){
					rang=tabl[i];
					tabl[i]=tabl[j];
					tabl[j]=rang;
				}
			}
		}
		for(i=0;i<50;i++){
		printf("%d\n",tabl[i]);}
		
		//TPOS ET TNEG
		p=0;
		g=0;
		k=0;
		l=0;
		for(i=0;i<50;i++){
			if(tabl[i]>0){
				tpos[k]=tabl[i];
				p++;
				k++;
			
			} 
			if(tabl[i]<0){
				tneg[l]=tabl[i];
				g++;
				l++;
			
			}
		}
		for(k=0;k<p;k++){
		printf("pos : %d\n",tpos[k]);}
		
		for(l=0;l<g;l++){
		printf("neg : %d\n",tneg[l]);}
		//={1,2541,51,15,51,154,-415,4,1,41-4,-694,-416,4,45,-49,-74,-465,4,-49,-4,-945,49,49,4-49,-94,94,-49,-49,4,79,41,1,-98,7,48,47,54,-49,49,-496,-49,45,44,496,49,-49,49,49}
 }
