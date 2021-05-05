:mod:`hub` -- Hub brick functionality
=====================================

Classes and functions related to simple parts and abilities of the Hub brick
itself, like buttons, ports, and internal sensors.

Raw module data
---------------

::

    object <module 'hub'> is of type module
      __name__ -- hub
      __version__ -- v1.0.06.0034-b0c335b
      info -- <function>
      power_off -- <function>
      repl_restart -- <function>
      Image -- <class 'Image'>
      status -- <function>
      port -- <class 'Port'>
      display -- <Display>
      button -- <class 'Button'>
      led -- <function>
      sound -- Sound()
      temperature -- <function>
      motion -- Motion()
      battery -- Battery class
      bluetooth -- <bt>
      ble -- <bluetooth>
      supervision -- <supervision>
      USB_VCP -- <class 'USB_VCP'>
      BT_VCP -- <class 'BT_VCP'>
      file_transfer -- <function>
    object <class 'BT_VCP'> is of type type
      setinterrupt -- <function>
      isconnected -- <function>
      any -- <function>
      send -- <function>
      recv -- <function>
      read -- <function>
      readinto -- <function>
      readline -- <function>
      readlines -- <function>
      write -- <function>
      close -- <function>
      __del__ -- <function>
      __enter__ -- <function>
      __exit__ -- <function>
      callback -- <function>
    object <class 'USB_VCP'> is of type type
      init -- <function>
      setinterrupt -- <function>
      isconnected -- <function>
      any -- <function>
      send -- <function>
      recv -- <function>
      read -- <function>
      readinto -- <function>
      readline -- <function>
      readlines -- <function>
      write -- <function>
      close -- <function>
      __del__ -- <function>
      __enter__ -- <function>
      __exit__ -- <function>
      callback -- <function>
      RTS -- 1
      CTS -- 2
    object <supervision> is of type supervision
      info -- <function>
    object <bluetooth> is of type bluetooth
      rssi -- <function>
      mac -- <function>
      scan -- <function>
      scan_result -- <function>
      connect -- <function>
      callback -- <function>
    object <bt> is of type bt
      info -- <function>
      discoverable -- <function>
    object Battery class is of type Battery
      BATTERY_NO_ERROR -- 0
      BATTERY_HUB_TEMPERATURE_CRITICAL_OUT_OF_RANGE -- -2
      BATTERY_TEMPERATURE_OUT_OF_RANGE -- -2
      BATTERY_TEMPERATURE_SENSOR_FAIL -- -3
      BATTERY_BAD_BATTERY -- -4
      BATTERY_VOLTAGE_TOO_LOW -- -5
      USB_CH_PORT_NONE -- 0
      USB_CH_PORT_SDP -- 1
      USB_CH_PORT_CDP -- 2
      USB_CH_PORT_DCP -- 3
      CHARGER_STATE_FAIL -- -1
      CHARGER_STATE_DISCHARGING -- 0
      CHARGER_STATE_CHARGING_ONGOING -- 1
      CHARGER_STATE_CHARGING_COMPLETED -- 2
      voltage -- <function>
      current -- <function>
      temperature -- <function>
      charger_detect -- <function>
      info -- <function>
      capacity_left -- <function>
    object Motion() is of type Motion
      NONE -- NULL
      LEFTSIDE -- leftside
      RIGHTSIDE -- rightside
      DOWN -- down
      UP -- up
      FRONT -- front
      BACK -- back
      TAPPED -- tapped
      DOUBLETAPPED -- doubletapped
      SHAKE -- shake
      FREEFALL -- freefall
      gyroscope -- <function>
      gyroscope_filter -- <function>
      accelerometer -- <function>
      accelerometer_filter -- <function>
      position -- <function>
      reset_yaw -- <function>
      preset_yaw -- <function>
      orientation -- <function>
      gesture -- <function>
      was_gesture -- <function>
      callback -- <function>
    object Sound() is of type Sound
      SOUND_SIN -- 0
      SOUND_SQUARE -- 1
      SOUND_TRIANGLE -- 2
      SOUND_SAWTOOTH -- 3
      volume -- <function>
      beep -- <function>
      play -- <function>
      callback -- <function>
    object <class 'Button'> is of type type
      center -- center
      left -- left
      right -- right
      connect -- connect
    object center is of type
      is_pressed -- <function>
      was_pressed -- <function>
      presses -- <function>
      callback -- <function>
      on_change -- <function>
    object left is of type
      is_pressed -- <function>
      was_pressed -- <function>
      presses -- <function>
      callback -- <function>
      on_change -- <function>
    object right is of type
      is_pressed -- <function>
      was_pressed -- <function>
      presses -- <function>
      callback -- <function>
      on_change -- <function>
    object connect is of type
      is_pressed -- <function>
      was_pressed -- <function>
      presses -- <function>
      callback -- <function>
      on_change -- <function>
    object <Display> is of type Display
      pixel -- <function>
      show -- <function>
      callback -- <function>
      clear -- <function>
      rotation -- <function>
    object <class 'Port'> is of type type
      DETACHED -- 0
      ATTACHED -- 1
      A -- Port(A)
      B -- Port(B)
      C -- Port(C)
      D -- Port(D)
      E -- Port(E)
      F -- Port(F)
      MODE_DEFAULT -- 0
      MODE_FULL_DUPLEX -- 1
      MODE_HALF_DUPLEX -- 2
      MODE_GPIO -- 3
    object Port(A) is of type Port
      callback -- <function>
      info -- <function>
      mode -- <function>
      pwm -- <function>
      device -- None
      motor -- None
    object <class 'Image'> is of type type
      width -- <function>
      height -- <function>
      get_pixel -- <function>
      set_pixel -- <function>
      shift_left -- <function>
      shift_right -- <function>
      shift_up -- <function>
      shift_down -- <function>
      HEART -- Image(
        '09090:'
        '99999:'
        '99999:'
        '09990:'
        '00900:'
    )
      HEART_SMALL -- Image(
        '00000:'
        '09090:'
        '09990:'
        '00900:'
        '00000:'
    )
      HAPPY -- Image(
        '00000:'
        '09090:'
        '00000:'
        '90009:'
        '09990:'
    )
      SMILE -- Image(
        '00000:'
        '00000:'
        '00000:'
        '90009:'
        '09990:'
    )
      SAD -- Image(
        '00000:'
        '09090:'
        '00000:'
        '09990:'
        '90009:'
    )
      CONFUSED -- Image(
        '00000:'
        '09090:'
        '00000:'
        '09090:'
        '90909:'
    )
      ANGRY -- Image(
        '90009:'
        '09090:'
        '00000:'
        '99999:'
        '90909:'
    )
      ASLEEP -- Image(
        '00000:'
        '99099:'
        '00000:'
        '09990:'
        '00000:'
    )
      SURPRISED -- Image(
        '09090:'
        '00000:'
        '00900:'
        '09090:'
        '00900:'
    )
      SILLY -- Image(
        '90009:'
        '00000:'
        '99999:'
        '00909:'
        '00999:'
    )
      FABULOUS -- Image(
        '99999:'
        '99099:'
        '00000:'
        '09090:'
        '09990:'
    )
      MEH -- Image(
        '09090:'
        '00000:'
        '00090:'
        '00900:'
        '09000:'
    )
      YES -- Image(
        '00000:'
        '00009:'
        '00090:'
        '90900:'
        '09000:'
    )
      NO -- Image(
        '90009:'
        '09090:'
        '00900:'
        '09090:'
        '90009:'
    )
      CLOCK12 -- Image(
        '00900:'
        '00900:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK1 -- Image(
        '00090:'
        '00090:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK2 -- Image(
        '00000:'
        '00099:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK3 -- Image(
        '00000:'
        '00000:'
        '00999:'
        '00000:'
        '00000:'
    )
      CLOCK4 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00099:'
        '00000:'
    )
      CLOCK5 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00090:'
        '00090:'
    )
      CLOCK6 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00900:'
        '00900:'
    )
      CLOCK7 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '09000:'
        '09000:'
    )
      CLOCK8 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '99000:'
        '00000:'
    )
      CLOCK9 -- Image(
        '00000:'
        '00000:'
        '99900:'
        '00000:'
        '00000:'
    )
      CLOCK10 -- Image(
        '00000:'
        '99000:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK11 -- Image(
        '09000:'
        '09000:'
        '00900:'
        '00000:'
        '00000:'
    )
      ARROW_N -- Image(
        '00900:'
        '09990:'
        '90909:'
        '00900:'
        '00900:'
    )
      ARROW_NE -- Image(
        '00999:'
        '00099:'
        '00909:'
        '09000:'
        '90000:'
    )
      ARROW_E -- Image(
        '00900:'
        '00090:'
        '99999:'
        '00090:'
        '00900:'
    )
      ARROW_SE -- Image(
        '90000:'
        '09000:'
        '00909:'
        '00099:'
        '00999:'
    )
      ARROW_S -- Image(
        '00900:'
        '00900:'
        '90909:'
        '09990:'
        '00900:'
    )
      ARROW_SW -- Image(
        '00009:'
        '00090:'
        '90900:'
        '99000:'
        '99900:'
    )
      ARROW_W -- Image(
        '00900:'
        '09000:'
        '99999:'
        '09000:'
        '00900:'
    )
      ARROW_NW -- Image(
        '99900:'
        '99000:'
        '90900:'
        '00090:'
        '00009:'
    )
      GO_RIGHT -- Image(
        '09000:'
        '09900:'
        '09990:'
        '09900:'
        '09000:'
    )
      GO_LEFT -- Image(
        '00090:'
        '00990:'
        '09990:'
        '00990:'
        '00090:'
    )
      GO_UP -- Image(
        '00000:'
        '00900:'
        '09990:'
        '99999:'
        '00000:'
    )
      GO_DOWN -- Image(
        '00000:'
        '99999:'
        '09990:'
        '00900:'
        '00000:'
    )
      TRIANGLE -- Image(
        '00000:'
        '00900:'
        '09090:'
        '99999:'
        '00000:'
    )
      TRIANGLE_LEFT -- Image(
        '90000:'
        '99000:'
        '90900:'
        '90090:'
        '99999:'
    )
      CHESSBOARD -- Image(
        '09090:'
        '90909:'
        '09090:'
        '90909:'
        '09090:'
    )
      DIAMOND -- Image(
        '00900:'
        '09090:'
        '90009:'
        '09090:'
        '00900:'
    )
      DIAMOND_SMALL -- Image(
        '00000:'
        '00900:'
        '09090:'
        '00900:'
        '00000:'
    )
      SQUARE -- Image(
        '99999:'
        '90009:'
        '90009:'
        '90009:'
        '99999:'
    )
      SQUARE_SMALL -- Image(
        '00000:'
        '09990:'
        '09090:'
        '09990:'
        '00000:'
    )
      RABBIT -- Image(
        '90900:'
        '90900:'
        '99990:'
        '99090:'
        '99990:'
    )
      COW -- Image(
        '90009:'
        '90009:'
        '99999:'
        '09990:'
        '00900:'
    )
      MUSIC_CROTCHET -- Image(
        '00900:'
        '00900:'
        '00900:'
        '99900:'
        '99900:'
    )
      MUSIC_QUAVER -- Image(
        '00900:'
        '00990:'
        '00909:'
        '99900:'
        '99900:'
    )
      MUSIC_QUAVERS -- Image(
        '09999:'
        '09009:'
        '09009:'
        '99099:'
        '99099:'
    )
      PITCHFORK -- Image(
        '90909:'
        '90909:'
        '99999:'
        '00900:'
        '00900:'
    )
      XMAS -- Image(
        '00900:'
        '09990:'
        '00900:'
        '09990:'
        '99999:'
    )
      PACMAN -- Image(
        '09999:'
        '99090:'
        '99900:'
        '99990:'
        '09999:'
    )
      TARGET -- Image(
        '00900:'
        '09990:'
        '99099:'
        '09990:'
        '00900:'
    )
      ALL_CLOCKS -- (Image('00900:00900:00900:00000:00000:'), Image('00090:00090:00900:00000:00000:'), Image('00000:00099:00900:00000:00000:'), Image('00000:00000:00999:00000:00000:'), Image('00000:00000:00900:00099:00000:'), Image('00000:00000:00900:00090:00090:'), Image('00000:00000:00900:00900:00900:'), Image('00000:00000:00900:09000:09000:'), Image('00000:00000:00900:99000:00000:'), Image('00000:00000:99900:00000:00000:'), Image('00000:99000:00900:00000:00000:'), Image('09000:09000:00900:00000:00000:'))
      ALL_ARROWS -- (Image('00900:09990:90909:00900:00900:'), Image('00999:00099:00909:09000:90000:'), Image('00900:00090:99999:00090:00900:'), Image('90000:09000:00909:00099:00999:'), Image('00900:00900:90909:09990:00900:'), Image('00009:00090:90900:99000:99900:'), Image('00900:09000:99999:09000:00900:'), Image('99900:99000:90900:00090:00009:'))
      TSHIRT -- Image(
        '99099:'
        '99999:'
        '09990:'
        '09990:'
        '09990:'
    )
      ROLLERSKATE -- Image(
        '00099:'
        '00099:'
        '99999:'
        '99999:'
        '09090:'
    )
      DUCK -- Image(
        '09900:'
        '99900:'
        '09999:'
        '09990:'
        '00000:'
    )
      HOUSE -- Image(
        '00900:'
        '09990:'
        '99999:'
        '09990:'
        '09090:'
    )
      TORTOISE -- Image(
        '00000:'
        '09990:'
        '99999:'
        '09090:'
        '00000:'
    )
      BUTTERFLY -- Image(
        '99099:'
        '99999:'
        '00900:'
        '99999:'
        '99099:'
    )
      STICKFIGURE -- Image(
        '00900:'
        '99999:'
        '00900:'
        '09090:'
        '90009:'
    )
      GHOST -- Image(
        '99999:'
        '90909:'
        '99999:'
        '99999:'
        '90909:'
    )
      SWORD -- Image(
        '00900:'
        '00900:'
        '00900:'
        '09990:'
        '00900:'
    )
      GIRAFFE -- Image(
        '99000:'
        '09000:'
        '09000:'
        '09990:'
        '09090:'
    )
      SKULL -- Image(
        '09990:'
        '90909:'
        '99999:'
        '09990:'
        '09990:'
    )
      UMBRELLA -- Image(
        '09990:'
        '99999:'
        '00900:'
        '90900:'
        '09900:'
    )
      SNAKE -- Image(
        '99000:'
        '99099:'
        '09090:'
        '09990:'
        '00000:'
    )