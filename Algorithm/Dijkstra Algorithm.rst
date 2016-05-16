Dijkstra Algorithm(다익스트라 알고리즘)
=============================
가중치가 있는 그래프에서 최단경로를 찾는 알고리즘

.. image:: Algorithm/image/dijkstar0.jpg

graph = {'집':{'학원':9, '슈퍼마켓':10, '미용실':5},
         '미용실':{'슈퍼마켓':3, '은행':11, '집':5},
         '슈퍼마켓':{'레스토랑':3, '학원':7, '은행':10, '미용실':3, '집':10},
         '레스토랑':{'은행':4, '슈퍼마켓':3},
         '은행':{'학교':2, '학원':7, '미용실':11, '슈퍼마켓':10, '레스토랑':4},
         '학교':{'은행':2, '학원':12},
         '학원':{'집':9, '슈퍼마켓':7, '은행':7, '학교':12}}

def Dijkstra(graph,start,end):
    router=dict()
    for keys in graph.keys():
        router[keys] = {'dist':'infinit', 'route':[], 'visit':0}

    for keys in graph[start].keys():
        router[keys]['dist'] = graph[start][keys]
        router[keys]['route'] = [start]

    router[start]['visit'] = 1
    router[start]['dist'] = 0

# visit이 0인것중에 가장 짧은것 while
    while 1:
        # print("not router[k]['visit']")
        not_visit = {k:router[k]['dist'] for k in router.keys() if router[k]['visit']==0 if router[k]['dist'] != 'infinit'}
        # print(not_visit)
        if not not_visit:
            break
        for k in not_visit.keys():
            if not_visit[k] == min(not_visit.values()):
                print(k)
                router[k]['visit']=1
                for going in graph[k].keys():
                    if router[going]['dist'] !=0:
                        if router[going]['dist']!='infinit' and router[going]['dist']> router[k]['dist'] + graph[k][going]:
                            router[going]['dist'] = router[k]['dist'] + graph[k][going]
                            router[going]['route'] = router[k]['route'] +[k]

                        elif router[going]['dist'] =='infinit':
                            router[going]['dist'] = router[k]['dist'] + graph[k][going]
                            router[going]['route'] = router[k]['route'] + [k]

    print("{}에서 {}까지 최단경로는 ".format(start,end),end='')
    for p in router[end]['route']:
        print(p,end='->')
    print(end)
    print("최단 거리는 {}".format(router[end]['dist']))

Dijkstra(graph,'집','학교')

