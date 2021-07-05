# 查询对象字段后缀汇总

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x540E;&#x7F00;&#x540D;&#x79F0;</th>
      <th style="text-align:left">&#x64CD;&#x4F5C;&#x7B26;</th>
      <th style="text-align:left">&#x5360;&#x4F4D;&#x7B26;</th>
      <th style="text-align:left">&#x7C7B;&#x578B;&#x9650;&#x5236;</th>
      <th style="text-align:left">&#x503C;&#x5904;&#x7406;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">-</td>
      <td style="text-align:left">=</td>
      <td style="text-align:left">&#xFF1F;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Not</td>
      <td style="text-align:left">!=</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">NotLike</td>
      <td style="text-align:left">NOT LIKE</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">%value%</td>
    </tr>
    <tr>
      <td style="text-align:left">Like</td>
      <td style="text-align:left">LIKE</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">%value%</td>
    </tr>
    <tr>
      <td style="text-align:left">Start</td>
      <td style="text-align:left">LIKE</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">%value</td>
    </tr>
    <tr>
      <td style="text-align:left">NotIn</td>
      <td style="text-align:left">NOT IN</td>
      <td style="text-align:left">(?[, ?]+)</td>
      <td style="text-align:left">Collection</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">In</td>
      <td style="text-align:left">IN</td>
      <td style="text-align:left">
        <p>(?[, ?]+)</p>
        <p>(null)</p>
      </td>
      <td style="text-align:left">Collection</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">NotNull</td>
      <td style="text-align:left">IS NOT NULL</td>
      <td style="text-align:left">-</td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Null</td>
      <td style="text-align:left">IS NULL</td>
      <td style="text-align:left">-</td>
      <td style="text-align:left">boolean</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Gt</td>
      <td style="text-align:left">&gt;</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Ge</td>
      <td style="text-align:left">&gt;=</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Lt</td>
      <td style="text-align:left">&lt;</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Le</td>
      <td style="text-align:left">&lt;=</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Eq</td>
      <td style="text-align:left">=</td>
      <td style="text-align:left">?</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>



