# WebSocket

 useEffect(() => {
 
    const ws = new WebSocket("wss://websocket-8jxu.onrender.com");

 
    ws.onmessage = (event) => {
      const data = JSON.parse(event.data);
      setActiveUsers(data.activeUsers);
    };

    return () => {
      ws.close();
    };
  }, []);
