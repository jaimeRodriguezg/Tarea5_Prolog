distancia(beast_dean,deepnest, 8).
distancia(deepnest,fungal, 10).
distancia(fungal,waterways,10).
distancia(fungal,garden,16).
distancia(fungal,canyon,3).
distancia(fungal,crossroad,5).
distancia(garden,canyon,12).
distancia(canyon,greenpath,10).
distancia(greenpath,crossroad,4).
distancia(crossroad,dirthmouth,1).
distancia(crossroad,city_of_tears,4).
distancia(crossroad,blue_lake,2).
distancia(dirthmouth,crystal_peak,5).
distancia(waterways,city_of_tears,7).
distancia(crystal_peak,resting_grounds,8).
distancia(blue_lake,resting_grounds,3).
distancia(city_of_tears,resting_grounds,3).
distancia(waterways,edge,6).
distancia(edge,resting_grounds,14).
distancia(edge,hive,3).
distinto(X,Y):-not(X=Y).
directos(C,X,T):-distancia(C,X,Z),Z=<T.
directos(C,X,T):-distancia(X,C,Z),Z=<T.
indirectos(C,X,T):-distancia(C,Y,T1),directos(Y,X,T-T1).
indirectos(C,X,T):-distancia(Y,C,T1),directos(X,Y,T-T1).
posible(C,X,T):-(directos(C,X,T),distinto(C,X));(indirectos(C,X,T),distinto(C,X)).
alcanzable(C,T,L):-findall(X,posible(C,X,T),L_aux),sort(L_aux,L).
