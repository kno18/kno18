pestaña de función = newmod (x_0, tole, n, f, d, d_2)
	  formato largo
	  fx = en línea (f);
	  fd = en línea (d);
	  fdd = en línea (d_2);
	  j = 0;
	  error = tole + 1;
	  
	  while error> toles & j <n
	    y = fx (x_0);
	    yd = fd (x_0);
	    ydd = fdd (x_0);
	    x_1 = x_0- (y * yd) / (yd ^ 2-y-ydd);
	    error = abs (x_1-x_0);
	  
	    j = j + 1;
	    tabulador (j, 1) = j;
	    tabulador (j, 2) = x_0;
	    tab (j, 3) = y;
	    tab (j, 4) = yd;
	    tabulador (j, 5) = ydd;
	    tab (j, 6) = error;
	    tab (1,1) = 0;
	    x_0 = x_1;
	  
	  final
	  
	  si y == 0
	      fprintf ('% g es raiz. \ n.', x_0);
	    elseif error <tole
	                fprintf ('% g es aproximacion con una tolerancia =% gy un error =% g. \ n.', x_0, tole, error);
	                fprintf ('La función de actualización en ese punto es f (x) =% g. \ n.', y);
	                fprintf ('La derivada de la función de actualización en ese punto es d / dx =% g. \ n.', yd);
	                fprintf ('La segunda derivada de la función de actualización en ese punto es% g. \ n.', ydd);
	  demás
	                fprintf ('el metodo no funciono en n iteraciones');
			final
	final	

