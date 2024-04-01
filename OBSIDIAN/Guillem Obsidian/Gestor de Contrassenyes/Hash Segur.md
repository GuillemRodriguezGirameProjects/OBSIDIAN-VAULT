Per poder fer un Hash segur es necessiten les següents característiques:
- [ ] Funció per fer un HASH que no s'hagi trencat encara.
- [ ] Una Seed de la qual partirà el HASH
- [ ] Una funció de Salt i la seva Seed per poder fer el HASH restultant més difícil de trobat en el cas de que s'aconsegueixi un HASH igual fent un forçat extern.
- [ ] Una forma de poder replicar els passos fets servir per aconseguir el HASH de la contrassenya, per poder "descodificar-la". Això significa guardar d'alguna forma la Seed del HASH i de la Salt.

Realment només s'ha de guardar la Salt, ja que es podría fer servir la Pista que donaría el Client com a llavor pel HASH. Després la Salt podría ser alguna cosa com el temps del sistema en el moment en el que es crea la Contrassenya. 

Segons el diagrama [[Primera Idea del Hash de la Contrassenya.canvas|Primera Idea del Hash de la Contrassenya]] el Salt estaria guardat en les N últimes xifres del HASH Que es guardaría a la Base de Dades. De manera que si es busca aquestes xifres dins de la Key del Mapa<Hash, Contrassenya> ja es té el Salt per poder recrear el HASH.
