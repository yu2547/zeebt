<xml xmlns="http://www.w3.org/1999/xhtml" collection="false">
  <variables>
    <variable type="" id="NF4F:F)/OD%/WGw?#p21">LAST DIGIT</variable>
    <variable type="" id="hI@Y}s|lTxY^B?|ePQo3">MAXIMUM LOSS</variable>
    <variable type="" id="B1QULQFHhsY:UDFFic@Y">TARGET</variable>
    <variable type="" id="GYiy?v@WnvT%BAgL0J7S">STAKE</variable>
    <variable type="" id="F4wur(a=}{e-X~0WBkHA">WIN STAKE</variable>
    <variable type="" id="Y9Odb50J;.aLg825Z0Zu">MARTINGALE</variable>
  </variables>
  <block type="trade" id="73vWdDagX-YhN)CtN.3D" x="12" y="21">
    <field name="MARKET_LIST">synthetic_index</field>
    <field name="SUBMARKET_LIST">random_index</field>
    <field name="SYMBOL_LIST">R_75</field>
    <field name="TRADETYPECAT_LIST">digits</field>
    <field name="TRADETYPE_LIST">overunder</field>
    <field name="TYPE_LIST">DIGITOVER</field>
    <field name="CANDLEINTERVAL_LIST">60</field>
    <field name="TIME_MACHINE_ENABLED">FALSE</field>
    <field name="RESTARTONERROR">TRUE</field>
    <statement name="INITIALIZATION">
      <block type="variables_set" id="Zs12WS8wwSD$LoS,`J!x">
        <field name="VAR" id="hI@Y}s|lTxY^B?|ePQo3" variabletype="">MAXIMUM LOSS</field>
        <value name="VALUE">
          <block type="math_number" id="P1,cyQ}FtImbCZ|u+g5(">
            <field name="NUM">1000</field>
          </block>
        </value>
        <next>
          <block type="variables_set" id="D!qv#iHJ:ZOTG!8SBOM_">
            <field name="VAR" id="B1QULQFHhsY:UDFFic@Y" variabletype="">TARGET</field>
            <value name="VALUE">
              <block type="math_number" id="v;/qX-WI9G.g+.N^7ntq">
                <field name="NUM">7</field>
              </block>
            </value>
            <next>
              <block type="variables_set" id="@%fc)+|l*+9`u#[d{=]x">
                <field name="VAR" id="GYiy?v@WnvT%BAgL0J7S" variabletype="">STAKE</field>
                <value name="VALUE">
                  <block type="math_number" id="2%I5[QMh|XxR3$F?kybR">
                    <field name="NUM">0.65</field>
                  </block>
                </value>
                <next>
                  <block type="variables_set" id="G~lr5U;{3c`7RzoFoC`a">
                    <field name="VAR" id="F4wur(a=}{e-X~0WBkHA" variabletype="">WIN STAKE</field>
                    <value name="VALUE">
                      <block type="math_number" id="%qF_Giqb7;-cT3E(b;te">
                        <field name="NUM">0.46</field>
                      </block>
                    </value>
                    <next>
                      <block type="variables_set" id="~`Hy9.Hi3(PHx^1GaKWU">
                        <field name="VAR" id="Y9Odb50J;.aLg825Z0Zu" variabletype="">MARTINGALE</field>
                        <value name="VALUE">
                          <block type="math_number" id="-.IEm?;#llux):K@(jr6">
                            <field name="NUM">4.1</field>
                          </block>
                        </value>
                        <next>
                          <block type="variables_set" id="0WE8tUNlSZx3}cR%JAi:">
                            <field name="VAR" id="NF4F:F)/OD%/WGw?#p21" variabletype="">LAST DIGIT</field>
                            <value name="VALUE">
                              <block type="math_number" id="{${:[Pm,sK[ak5*W8Q34">
                                <field name="NUM">2</field>
                              </block>
                            </value>
                            <next>
                              <block type="notify" id="_0h-Zg.=]5sv1^hIq8o[" collapsed="true">
                                <field name="NOTIFICATION_TYPE">info</field>
                                <field name="NOTIFICATION_SOUND">announcement</field>
                                <value name="MESSAGE">
                                  <shadow type="text" id="GBhaChEk)H,SfoLK.8Z^">
                                    <field name="TEXT">abc</field>
                                  </shadow>
                                  <block type="text" id="z4dc++laOBG@5E.1LSxq" collapsed="true">
                                    <field name="TEXT">Created by: Dboty (pbinarybot@gmail.com)</field>
                                  </block>
                                </value>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
    <statement name="SUBMARKET">
      <block type="tradeOptions" id="IEra)5~tI=N9mCmxLi(X">
        <field name="DURATIONTYPE_LIST">t</field>
        <field name="CURRENCY_LIST">USD</field>
        <field name="BARRIEROFFSETTYPE_LIST">+</field>
        <field name="SECONDBARRIEROFFSETTYPE_LIST">-</field>
        <value name="DURATION">
          <block type="math_number" id="*Z{D2jDqE|OvVHOU~v!I">
            <field name="NUM">1</field>
          </block>
        </value>
        <value name="AMOUNT">
          <block type="variables_get" id="1|0b~nTFQhQ~H,cG!):6" collapsed="true">
            <field name="VAR" id="GYiy?v@WnvT%BAgL0J7S" variabletype="">STAKE</field>
          </block>
        </value>
        <value name="PREDICTION">
          <shadow type="math_number" id="waUAjB,oWhn2XZcDparx">
            <field name="NUM">1</field>
          </shadow>
        </value>
      </block>
    </statement>
  </block>
  <block type="during_purchase" id="(4;NieXd}j|Bn!c-YiC|" x="644" y="517">
    <statement name="DURING_PURCHASE_STACK">
      <block type="controls_if" id="8?eYKAW%VczmRXQ-ou3r">
        <value name="IF0">
          <block type="check_sell" id="M=:_KpEeRAJY_}XTU^8~"></block>
        </value>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="tOc)]Xd=cAm0aiy+-8(8" x="0" y="643">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="timeout" id="]_Q$hDiPo[}fCBM%lEIi">
        <statement name="TIMEOUTSTACK">
          <block type="controls_if" id="J}yW|D?@tZ7yXM{),8W,">
            <mutation elseif="4"></mutation>
            <value name="IF0">
              <block type="logic_compare" id="?LxZC*50DqBUCy/o;6m=">
                <field name="OP">EQ</field>
                <value name="A">
                  <block type="last_digit" id="7@[A*e^91;9O69jbJfUi"></block>
                </value>
                <value name="B">
                  <block type="math_number" id="3`dJ;^^@u:BcmG%-MXWe">
                    <field name="NUM">5</field>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO0">
              <block type="notify" id="Kmq=k9(=wu?m]KggAAka">
                <field name="NOTIFICATION_TYPE">info</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="c9WgC[*uUIQ8x?hYIm5x">
                    <field name="TEXT">Digit 0</field>
                  </shadow>
                </value>
                <next>
                  <block type="variables_set" id="t#v-)P:}Y,+p!c)c-;zD">
                    <field name="VAR" id="NF4F:F)/OD%/WGw?#p21" variabletype="">LAST DIGIT</field>
                    <value name="VALUE">
                      <block type="math_number" id="^=-o4ThSL;2F/aoOoKzm">
                        <field name="NUM">0</field>
                      </block>
                    </value>
                    <next>
                      <block type="purchase" id="lBVihhVdMt[AXg8Q~sQD">
                        <field name="PURCHASE_LIST">DIGITOVER</field>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
            <value name="IF1">
              <block type="logic_compare" id="$IuLu@WT,X!8HuAsgU0J">
                <field name="OP">EQ</field>
                <value name="A">
                  <block type="last_digit" id="D9o49aUHKAyis8)9-B$E"></block>
                </value>
                <value name="B">
                  <block type="math_number" id=":7`D#KITjOwA?;]}SR/!">
                    <field name="NUM">6</field>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO1">
              <block type="notify" id=")%gd%O5xG_464;RX6GGT">
                <field name="NOTIFICATION_TYPE">info</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="vhzMXT,)wg`zKuF6=2mL">
                    <field name="TEXT">Digit 1</field>
                  </shadow>
                </value>
                <next>
                  <block type="variables_set" id="$m2mVBb)#3co@bZP/TEY">
                    <field name="VAR" id="NF4F:F)/OD%/WGw?#p21" variabletype="">LAST DIGIT</field>
                    <value name="VALUE">
                      <block type="math_number" id="CSooQwjF,X|-fMn*B:D/">
                        <field name="NUM">1</field>
                      </block>
                    </value>
                    <next>
                      <block type="purchase" id="[JMWqICq[a}:rxMp~aG1">
                        <field name="PURCHASE_LIST">DIGITOVER</field>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
            <value name="IF2">
              <block type="logic_compare" id="@N_MD9C|qhjBrxoED`4B">
                <field name="OP">EQ</field>
                <value name="A">
                  <block type="last_digit" id="gai=PR6cnV8V+oxL6n]B"></block>
                </value>
                <value name="B">
                  <block type="math_number" id="I(x]Tal?]7+YS:w@~|(Q">
                    <field name="NUM">7</field>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO2">
              <block type="notify" id="_iEQ?%N(5}:65]AA+#`v">
                <field name="NOTIFICATION_TYPE">info</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="}sT]E+6b;K8lhnbO!~%x">
                    <field name="TEXT">Digit 2</field>
                  </shadow>
                </value>
                <next>
                  <block type="variables_set" id="8L_0Y3j*vr[LETbO})m9">
                    <field name="VAR" id="NF4F:F)/OD%/WGw?#p21" variabletype="">LAST DIGIT</field>
                    <value name="VALUE">
                      <block type="math_number" id="CrzP;BBpp#j1Y}GI-%6K">
                        <field name="NUM">2</field>
                      </block>
                    </value>
                    <next>
                      <block type="purchase" id="f{OfyU~pY.fDQZB[BG/q" collapsed="true">
                        <field name="PURCHASE_LIST">DIGITOVER</field>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
            <value name="IF3">
              <block type="logic_compare" id="b}dA+7]-Pg6.QiL:;vZ(">
                <field name="OP">EQ</field>
                <value name="A">
                  <block type="last_digit" id="CTlrf~`vcDi+d4$}oKAD"></block>
                </value>
                <value name="B">
                  <block type="math_number" id="gv~IQ{oBM^mr5`Kz|u-*">
                    <field name="NUM">8</field>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO3">
              <block type="notify" id="HLkI3i3=;#;}_dSuh/3{">
                <field name="NOTIFICATION_TYPE">info</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="ui-youn]@$~!4BNsNwto">
                    <field name="TEXT">Digit 3</field>
                  </shadow>
                </value>
                <next>
                  <block type="variables_set" id="|WJ9bMeBM?e6fQ)|FxT7">
                    <field name="VAR" id="NF4F:F)/OD%/WGw?#p21" variabletype="">LAST DIGIT</field>
                    <value name="VALUE">
                      <block type="math_number" id="f9/R(1w8YmAGq|wiY5l%">
                        <field name="NUM">3</field>
                      </block>
                    </value>
                    <next>
                      <block type="purchase" id="G,Xv7%`1RjKYb6,DdPIw" collapsed="true">
                        <field name="PURCHASE_LIST">DIGITOVER</field>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
            <value name="IF4">
              <block type="logic_compare" id="k38S+):n$ki|9$BDgLwc">
                <field name="OP">EQ</field>
                <value name="A">
                  <block type="last_digit" id="3,[)@EEzU3ebH*BUw(l^"></block>
                </value>
                <value name="B">
                  <block type="math_number" id="(enA{Vfwa]P)uEGqN[uj">
                    <field name="NUM">9</field>
                  </block>
                </value>
              </block>
            </value>
            <statement name="DO4">
              <block type="notify" id="{((b^gn:KDCu!9FK;[){">
                <field name="NOTIFICATION_TYPE">info</field>
                <field name="NOTIFICATION_SOUND">silent</field>
                <value name="MESSAGE">
                  <shadow type="text" id="6}IrxUb!WqGE(1ihT5o]">
                    <field name="TEXT">Digit 4</field>
                  </shadow>
                </value>
                <next>
                  <block type="variables_set" id="9`fhY1JA7#cChZH/,kO^">
                    <field name="VAR" id="NF4F:F)/OD%/WGw?#p21" variabletype="">LAST DIGIT</field>
                    <value name="VALUE">
                      <block type="math_number" id="TF@J9kD+gn4_*4wFEXH`">
                        <field name="NUM">4</field>
                      </block>
                    </value>
                    <next>
                      <block type="purchase" id="HcwUonE*HFqUAhhf%E:/" collapsed="true">
                        <field name="PURCHASE_LIST">DIGITOVER</field>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
            <next>
              <block type="controls_if
