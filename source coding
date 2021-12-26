public OnPlayerConnect(playerid)
{
      new  country[MAX_PLAYERS], city[MAX_PLAYERS];
    GetPlayerCountry(playerid, country, MAX_PLAYER_NAME);
    GetPlayerCity(playerid, city, MAX_PLAYER_NAME);
     foreach(new ii : Player)
            {
                    if(pInfo[ii][Logged] == 0)
                    {
                      //if(pInfo[ii][TogLoginNotif] == true)
                      SendClientMessageEx(ii, COLOR_RED, "* {00ffff}CONNECTED{FFFFFF}: "COL_WHITE" has connected to {79EEF7}Your Own Life Roleplay ({FFB60D}%s, %s{ffffff})", pInfo[playerid][Nick], playerid, city, country);                      
                      //return 1;
                    }
            }
}

public OnPlayerDisconnect(playerid, reason)
{
     pInfo[playerid][Logged] = 0;     
     new Float:x, Float:y, Float:z;
     GetPlayerPos(playerid, x, y, z);
      
      foreach(new ii : Player)
      {
        if(IsPlayerInRangeOfPoint(ii, 40.0, x, y, z))
        {
          //if(pInfo[ii][TogLoginNotif] == true)
          {
                        switch(reason)
                       {
                        case 0:
                        {

                          SendClientMessageEx(ii, COLOR_RED, "[SERVER]"COL_YELLOW" %s(%d) has leave from the server.(timeout/crash)", pInfo[playerid][Nick], playerid);
                        }
                        case 1:
                        {
                          SendClientMessageEx(ii, COLOR_RED, "[SERVER]"COL_YELLOW" %s(%d) has leave from the server.(leaving)", pInfo[playerid][Nick], playerid);
                        }
                        case 2:
                        {
                          SendClientMessageEx(ii, COLOR_RED, "[SERVER]"COL_YELLOW" %s(%d) has leave from the server.(kicked/banned)", pInfo[playerid][Nick], playerid);
                        }
                      }

          }
         
        }
      }

}
