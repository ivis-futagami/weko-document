### ファセット検索

  - > 目的・用途

本機能は、ファセット検索機能を詳細に設定できる機能である。

  - > 利用方法

管理者は本画面でファセット検索として表示する項目を設定できる。

設定された項目をもとに、システムが集計を行い、Web側で各ファセット項目と該当するアイテムをグルーピングし、そのカウントした値を表示する。

利用者は各ファセット項目の中にあるグルーピングされた値を選択することで、絞り込まれたアイテムがアイテムリストに表示される。

  - > 利用可能なロール

<table>
<thead>
<tr class="header">
<th>ロール</th>
<th>システム<br />
管理者</th>
<th>リポジトリ<br />
管理者</th>
<th>コミュニティ<br />
管理者</th>
<th>登録ユーザー</th>
<th>一般ユーザー</th>
<th>ゲスト<br />
(未ログイン)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>利用可否</td>
<td>○</td>
<td>○</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - > 機能内容

(1) ファセット検索の一覧画面

  - 【Administration \> 設定（Setting） \> ファセット検索（Faceted Search）】を選択すると表示される。

  - 画面構成は以下の通り
    
      - 一覧（List）タブ
        
          - 設定されているファセット検索の項目のリストを表示する。メニューからファセット検索（Faceted Search）を選択すると本タブが表示される。一覧（List）の横にファセット項目数を（）表記する。
    
      - 作成（Create）タブ
        
          - ファセット検索する項目を作成する。　　…詳細は(3)に記載
    
      - フィルターを追加（Add Filter）
        
          - 一覧（List）タブにあるファセット検索の項目のリストを絞り込んで表示する。
    
      - 選択（With selected）
        
          - 一覧（List）タブにあるファセット検索の項目のリストについて、選択したファセット検索の項目を削除する。
    
      - Searchテキストボックス
        
          - キーワードを入力すると、一覧（List）タブにあるファセット検索の項目のリストから検索して表示する。

  - 一覧（List）タブ
    
      - 設定されているファセット検索の項目のリストを表示する。表の構成は以下の通り
        
          - チェックボックス
            
              - ファセット項目を選択できる。選択した項目に対して削除が可能（※選択（With selected）を参照）
        
          - \[目\]マーク
            
              - 選択することで該当のファセット項目の詳細画面に遷移する。　　  
                …詳細は(2)に記載
        
          - \[鉛筆\]マーク
            
              - 選択することで該当のファセット項目の編集画面に遷移する。　　  
                …詳細は(3)に記載
        
          - \[ゴミ箱\]マーク
            
              - 選択することで該当のファセット項目の削除画面に遷移する。　　  
                …詳細は(4)に記載
        
          - ID
            
              - ファセット項目を一意に決定するID。1から順に付与され、初期値としてID 1～7のファセット項目を用意している。
        
          - Item Name(EN)
            
              - ファセット項目の英語の名称
        
          - Item Name(JP)
            
              - ファセット項目の日本語の名称
        
          - UI
        
          - ファセット検索時のUI。
        
          - Mapping
            
              - ファセット項目で集計対象としているマッピングの設定
        
          - Active
            
              - Web画面上にファセット項目を表示しているかどうかを表す。\[レ\]マークが表示、\[－\]マークが非表示を表す。
    
      - 初期値としてファセット項目を用意している。詳細は以下の通り

| ID | Item Name(EN) | Item Name(JP) | Mapping                      | UI        | Active |
| -- | ------------- | ------------- | ---------------------------- | --------- | ------ |
| 1  | Data Language | デ一タの言語        | language                     | SelectBox | \[レ\]  |
| 2  | Access        | アクセス制限        | accessRights                 | SelectBox | \[レ\]  |
| 3  | Location      | 地域            | geoLocation.geoLocationPlace | SelectBox | \[レ\]  |
| 4  | Temporal      | 時間的範囲         | temporal                     | SelectBox | \[レ\]  |
| 5  | Topic         | トピック          | subject.value                | SelectBox | \[レ\]  |
| 6  | Distributor   | 配布者           | contributor.contributorName  | SelectBox | \[レ\]  |
| 7  | Data Type     | デ一タタイプ        | description.value            | SelectBox | \[レ\]  |

　　　　　　　※\[レ\]マークは、Web画面上にファセット項目を表示する設定になっていることを表す。

  - フィルターを追加（Add Filter）
    
      - クリックすると、以下のフィルターリストを表示する。フィルターリストからフィルターをクリックすると、当該フィルターの入力エリアが画面上に追加される。
        
          - ID
            
              - ファセット項目のIDでフィルターを行う。
            
              - 選択できる条件は以下の通り
                
                  - 等しい（equals）　　※初期値
                
                  - 等しくない（not equal）
                
                  - より大きい（greater than）
                
                  - より小さい（smaller than）
                
                  - 空（empty）
                
                  - 一覧にある（in list）
                
                  - 一覧にない（not in list）
        
          - Item Name(EN)
            
              - ファセット項目の英語の名称でフィルターを行う
            
              - 選択できる条件は以下の通り
                
                  - 含む（contains）　　※初期値
                
                  - 含まれていません（not contains）
                
                  - 等しい（equals）
                
                  - 等しくない（not equal）
                
                  - 空（empty）
                
                  - 一覧にある（in list）
                
                  - 一覧にない（not in list）
        
          - Item Name(JP)
            
              - ファセット項目の日本語の名称でフィルターを行う
            
              - 選択できる条件は以下の通り
                
                  - 含む（contains）　　※初期値
                
                  - 含まれていません（not contains）
                
                  - 等しい（equals）
                
                  - 等しくない（not equal）
                
                  - 空（empty）
                
                  - 一覧にある（in list）
                
                  - 一覧にない（not in list）
        
          - Mapping
            
              - ファセット項目のマッピングの設定でフィルターを行う
            
              - 選択できる条件は以下の通り
                
                  - 含む（contains）　　※初期値
                
                  - 含まれていません（not contains）
                
                  - 等しい（equals）
                
                  - 等しくない（not equal）
                
                  - 空（empty）
                
                  - 一覧にある（in list）
                
                  - 一覧にない（not in list）
        
          - UI
            
              - UIの設定でフィルターを行う。
            
              - 選択できる項目は以下の通り。
                
                  - 含む（contains）　　※初期値
                
                  - 含まれていません（not contains）
                
                  - 等しい（equals）
                
                  - 等しくない（not equal）
                
                  - 空（empty）
                
                  - 一覧にある（in list）
                
                  - 一覧にない（not in list）
        
          - Active
            
              - ファセット項目の表示／非表示でフィルターを行う
            
              - 選択できる条件は以下の通り
                
                  - 等しい（equals）　　※初期値
                
                  - 等しくない（not equal）
            
              - 設定できる値は以下の通り
                
                  - はい（Yes）
                
                  - いいえ（No）
    
      - 各フィルターでキーワードを入力後、"Enter"キーもしくは\[適用（Apply）\]ボタンを押下すると、各フィルターの条件で絞り込み検索が行われ、検索結果が画面上に表示される。  
        ※検索結果が無い場合は「表にはアイテムがありません。（There are no items in the table.）」と画面上に表示される
    
      - フィルターによる絞り込み後、\[フィルターをリセット（Reset Filters）\]ボタンを表示すると全ての絞り込みが解除され、最初の一覧（List）タブの状態となる。
    
      - 各フィルターは\[×\]ボタンで入力エリアから削除される。

  - 選択（With selected）
    
      - クリックすると、以下のリストを表示する。リストから削除（Delete）をクリックすると、削除処理を実行確認画面がポップアップする。
        
          - 削除（Delete）
            
              - 選択したファセット項目について削除処理を実行してよいかのメッセージをポップアップで表示する。
                
                  - ポップアップのメッセージ：　「選択したレコードを削除してもよろしいですか。（Are you sure you want to delete selected records?）」  
                    　\[OK\]:　選択したファセット項目を削除する。  
                    　\[キャンセル\]:　削除せずに一覧画面へ戻る。
            
              - ファセット項目を選択していない場合は、ファセット項目のリストから選択をする旨のメッセージをポップアップで表示する。
                
                  - ポップアップのメッセージ：　「少なくとも1つのレコードを選択してください。（Please select at least one record.）」  
                    　\[OK\]:　一覧画面へ戻る。

  - Searchテキストボックス
    
      - キーワードを入力して"Enter"キーを押下すると、入力したキーワードで絞り込み検索が行われ、検索結果が画面上に表示される。  
        ※検索結果が無い場合は「表にはアイテムがありません。（There are no items in the table.）」と画面上に表示される
    
      - キーワードに対し、すべての表の項目に対して部分一致検索を行う。
    
      - キーワードを入力して検索をした後、Searchエリア欄の\[×\]ボタンを表示すると全ての絞り込みが解除され、最初の一覧（List）タブの状態となる。

  - 一覧（List）タブを表示している場合は、登録されている（表示／非表示に関わらず）ファセット項目の数を、タブ上のカッコ内の数値で表示する  
    例えば、ファセット項目が９つ登録されている場合、タブには「一覧(9)」, 「List(9)」のように表示する。

  - 一覧（List）タブの順序は更新順(降順)となる。最後に更新をしたファセット項目はリストの一番下に表示される。

(2) ファセット検索の詳細画面

  - 一覧（List）タブにある各ファセット項目の\[目\]マークを選択することで、選択したファセット項目の詳細画面に遷移する。

  - 選択したファセット項目の詳細画面は 詳細（Details）タブ に表示される。

  - 詳細画面では以下の情報を表示する。
    
      - 項目名(英)（Item Name(EN)）
        
          - 選択したファセット項目の英語名称を表示する。
    
      - 項目名(日)（Item Name(JP)）
        
          - 選択したファセット項目の日本語名称を表示する。
    
      - マッピング（Mapping）
        
          - 選択したファセット項目で集計対象として設定されているマッピング情報を表示する。
    
      - カスタム集計（Custom Aggregations）
        
          - 選択したファセット項目で独自に集計対象として設定したマッピング情報を表示する。  
            表示方法は編集画面にある「Aggregations List」の形とする。
    
      - 表示/非表示（Display/Hide）
        
          - 選択したファセット項目がWeb画面上に表示されているかどうかの設定を表示する。  
            表示の場合は「表示（Display）」, 非表示の場合は「非表示（Hide）」と表示する。
    
      - 開閉状態
        
          - 選択したファセット項目のUIが開かれているかの設定を表示する。

(3) ファセット検索の新規作成・編集画面このセクションを編集

新規作成

  - 一覧（List）タブと並んでいる 作成（Create）タブ を選択することで、新規にファセット項目を作成する。

  - 入力できる内容は以下の通り
    
      - 項目名(英)（Item Name(EN)）
        
          - ファセット項目の英語名称を入力する。テキスト形式で必須項目である。  
            Web画面で日本語以外のページを表示した際に本項目の名称が表示される。
    
      - 項目名(日)（Item Name(JP)）
        
          - ファセット項目の日本語名称を表示する。テキスト形式で必須項目である。  
            Web画面で日本語ページを表示した際に本項目の名称が表示される。
    
      - マッピング（Mapping）
        
          - ファセット項目で集計対象とするマッピング情報を選択する。プルダウン形式(いずれか１つを選択)で必須項目である。  
            プルダウンで選択できるリストは、JPCOARの索引定義（/weko-schema-ui/weko\_schema\_ui/mappings/v6/weko/item-v1.0.0.json）に従う。
    
      - UI
        
          - ファセット検索時のUIを選択する。CheckboxList、SelectBox、RangeSliderの３種から選択する。ただし、RangeSliderについてはマッピングでtemporalを選択した時のみ選択可能となる。
    
      - 表示件数（Display Number）
        
          - UIがCheckboxList時のファセット内の選択肢を設定する数値。1\~99内の整数を入力する。範囲外の整数や整数ではない数、数字以外を入力した場合、「表示件数は1以上99以下の整数値で入力する必要があります。（Display Number must be an integer value from 1 to 99.）」というメッセージがポップアップ表示される。
    
      - カスタム集計（Custom Aggregations）
        
          - ファセット項目で独自に集計対象としてマッピング情報を設定する。設定内容は以下の通り
            
              - 集計一覧（Aggregations List）
                
                  - 独自に集計対象として設定したマッピング情報を「集計マッピング（Aggregation Mapping） - 集計値（Aggregation Value）」の形でリスト形式で表示する。リストの中の行を選択すると、集計マッピング（Aggregation Mapping）と集計値（Aggregation Value）が連動して、選択した行のマッピング情報を表示する。  
                    カスタム集計を設定する際は、集計マッピング（Aggregation Mapping）と集計値（Aggregation Value）は両方とも設定しなければならない。
            
              - 集計マッピング（Aggregation Mapping）
                
                  - 独自に集計対象とするマッピング情報を選択する。プルダウン形式(いずれか１つを選択)であり、プルダウンで選択できるリストは、"item-v1.0.0.json"に従う。
            
              - 集計値（Aggregation Value）
                
                  - 独自に集計対象とするマッピング情報の集計値を設定する。テキスト形式である。

> 【使い方】
> 
> 例１
> 
> 　集計マッピング（Aggregation Mapping）に"publish\_status"を、集計値（Aggregation Value）に"0"を設定した場合、
> 
> 　該当のファセット項目は、マッピングで選択した値　かつ　"publish\_status"が"0"　となっているアイテムを集計します。
> 
> 例２
> 
> 　集計マッピング（Aggregation Mapping）に"title"を、集計値（Aggregation Value）に"テスト"を設定した場合、
> 
> 　該当のファセット項目は、マッピングで選択した値　かつ　"title"が"テスト"(完全一致)　となっているアイテムを集計します。

  - 独自の集計対象として設定したマッピング情報は、以下のボタンで追加／削除ができる。
    
      - \[追加（Add）\]ボタン
        
          - 設定した集計マッピング（Aggregation Mapping）と集計値（Aggregation Value）を集計一覧（Aggregations List）に登録する。
    
    <!-- end list -->
    
      - \[削除（Delete）\]ボタン
        
          - 集計一覧（Aggregations List）のリストの行を選択後、ボタン押下で該当のマッピング情報を削除する。

<!-- end list -->

  - 表示/非表示（Display/Hide）
    
      - 対象のファセット項目をWeb画面上に表示するかどうかを設定する。  
        表示の場合は「表示（Display）」, 非表示の場合は「非表示（Hide）」のラジオボタンを選択する。初期値は「表示（Display）」である。

<!-- end list -->

  - 入力した内容で登録・更新する際は以下のボタンを押下する。
    
      - \[保存（Save）\]ボタン
        
          - 入力した内容を保存し、一覧（List）タブに遷移する。  
            新規に登録した場合は、一覧（List）タブのリストの一番下に表示される。既存のファセット項目を更新した場合は、更新した内容が一覧（List）タブのリストに表示される。
    
      - \[キャンセル（Cancel）\]ボタン
        
          - 入力中の内容を破棄し、一覧（List）タブに遷移する。

編集

  - 一覧（List）タブにある各ファセット項目の\[鉛筆\]マークを選択することで、選択したファセット項目の編集画面に遷移する

  - 編集画面は 編集（Edit）タブ に表示される

  - 画面構成は 作成（Create）タブ と同様。  
    画面遷移すると、選択したファセット項目に登録されている内容が各エリアに表示される

  - 入力できる内容やボタン押下時の動作は 新規作成 の記載内容を参照

エラーメッセージ

  - ファセット登録・編集時において、\[保存（Save）\]ボタン押下時にエラーチェックを行い、不適切なデータ登録をしないように制御を行う。

  - エラーメッセージはポップアップで画面上に表示される。  
    ポップアップ上の\[キャンセル（Cancel）\]ボタンを押下すると、ポップアップは消えて自画面を表示する（修正箇所は赤枠等で表示はされない）

  - 本画面でチェックしているエラー内容は以下の通り。

| エラー発生条件                                           | 表示されるエラーメッセージ                                                                                                                   |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 必須項目が入力されていない状態で保存しようとした場合                        | 必須項目は全て入力して下さい。（Please input all required item.）                                                                                |
| アイテム編集時、必須項目の中で既に存在している名称やマッピング情報がある状態で保存しようとした場合 | 既に存在する項目名・マッピングです。別のファセット項目名・マッピングを入力してください。（The item name/mapping is already exists. Please input other faceted item/mapping.） |
| 予期せぬエラーが発生した場合                                    | サーバエラーのため、作成に失敗しました（Failed to create due to server error.）                                                                      |

(4) ファセット検索の削除画面

  - 一覧（List）タブにある各ファセット項目の\[ゴミ箱\]マークを選択することで、選択したファセット項目の削除画面に遷移する

  - 削除画面は 削除（Delete）タブ に表示される

  - 画面遷移すると、選択したファセット項目に登録されている内容が表示される

  - 削除画面では以下の内容を表示する
    
      - 項目名(英)（Item Name(EN)）
        
          - 選択したファセット項目の英語名称を表示する
    
      - 項目名(日)（Item Name(JP)）
        
          - 選択したファセット項目の日本語名称を表示する
    
      - マッピング（Mapping）
        
          - 選択したファセット項目で集計対象として設定されているマッピング情報を表示する
    
      - カスタム集計（Custom Aggregations）
        
          - 選択したファセット項目で独自に集計対象として設定したマッピング情報を表示する  
            表示方法は編集画面にある「Aggregations List」の形とする
    
      - 表示/非表示（Display/Hide）
        
          - 選択したファセット項目がWeb画面上に表示されているかどうかを表示する  
            表示の場合は「表示（Display）」, 非表示の場合は「非表示（Hide）」と表示する

  - 削除画面では削除をする際は以下のボタンを押下する
    
      - \[削除（Delete）\]ボタン
        
          - ボタンを押下すると、選択したファセット項目について削除処理を実行してよいかのメッセージをポップアップで表示する。
            
              - ポップアップのメッセージ：　「選択したレコードを削除してもよろしいですか。（Are you sure you want to delete selected records?）」  
                　\[OK\]:　選択したファセット項目を削除する  
                　\[キャンセル\]:　削除せずに削除画面へ戻る
    
      - \[キャンセル（Cancel）\]ボタン
        
          - ボタンを押下すると、一覧（List）タブへ戻る

  - 予期せぬエラーが発生した場合、「サーバエラーのため、削除に失敗しました（Failed to delete due to server error.）」のポップアップを表示する  
    \[キャンセル（Cancel）\]ボタンを押下すると、自画面へ戻る

(5) その他

  - 表示している画面のタブから他のタブへ遷移できるもののリストは以下の通り

<table>
<thead>
<tr class="header">
<th>現在のタブ</th>
<th>→</th>
<th>遷移できるタブ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>一覧（List）</td>
<td>→</td>
<td>作成（Create）</td>
</tr>
<tr class="even">
<td>作成（Create）</td>
<td></td>
<td>一覧（List）</td>
</tr>
<tr class="odd">
<td>編集（Edit）</td>
<td></td>
<td>一覧（List）<br />
作成（Create）<br />
詳細（Details）　※編集（Edit）タブで表示しているファセット項目の詳細画面を表示する<br />
削除（Delete）　※編集（Edit）タブで表示しているファセット項目の削除画面を表示する</td>
</tr>
<tr class="even">
<td>詳細（Details）</td>
<td></td>
<td>一覧（List）<br />
作成（Create）<br />
編集（Edit）　　※詳細（Details）タブで表示しているファセット項目の編集画面を表示する<br />
削除（Delete）　※詳細（Details）タブで表示しているファセット項目の削除画面を表示する</td>
</tr>
<tr class="odd">
<td>削除（Delete）</td>
<td></td>
<td>一覧（List）<br />
作成（Create）<br />
編集（Edit）　　※削除（Delete）タブで表示しているファセット項目の編集画面を表示する<br />
詳細（Details）　※削除（Delete）タブで表示しているファセット項目の詳細画面を表示する</td>
</tr>
</tbody>
</table>

  - ファセット項目を表示する設定としているが、カスタム集計の集計マッピングが未入力のときに、Web画面でインデックスリストの選択と検索ができないため注意  
    (ファセットの表示設定ON/OFFに限らず発生)

<!-- end list -->

  - > 関連モジュール

<!-- end list -->

  - > weko\_admin

<!-- end list -->

  - > 処理概要

> 一覧表示

  - > weko\_admin.model.FacetSearchSetting.get\_allが呼び出され、db内のfacet\_search\_settingテーブルの全情報が取り出され表示されている。

  - > 任意のファセット項目の目のマークを押下すると、weko\_admin.admin.FacatSearchView.details\_viewが呼び出され、クリックしたファセット項目の詳細情報が、db内のfacet\_search\_settingテーブルから取り出され表示される。

  - > 任意のファセット項目の鉛筆マークを押下すると、weko\_admin.admin.FacatSearchView.edit\_viewが呼び出され編集画面へ移行し、\[保存(Save)\]ボタンを押下すると、 weko\_admin.views.save\_facet\_searchが呼び出され、編集内容に問題がなければ、db内のfacet\_search\_settingテーブルの情報が変更される。

  - > 任意のファセット項目のゴミ箱マークを押下すると、weko\_admin.admin.FacetSearchSettingView.deleteが呼び出され削除画面へ移行し、「削除（delete）」ボタンが押下されるとweko\_admin.views.remove\_facet\_searchが呼び出され、db内のfacet\_search\_settingテーブルから選択したファセット項目が削除される。

> 作成

  - > 作成タブを押下すると、weko\_admin.admin.FacetSearchSettingView.create\_viewが呼び出され、作成画面へ移行する。各種項目に作成するファセット項目の情報を入力し\[保存（Save）\]ボタンを押下すると、weko\_admin.views.save\_facet\_searchが呼び出され、入力項目に問題がなければ、db内のfacet\_search\_settingテーブルに入力情報が追加される。入力項目の規制については、上記の「(3) ファセット検索の新規作成・編集画面このセクションを編集」に示した通りである。

> 選択

  - > 一つ以上のファセット項目を選択した状態で、選択タブから削除を選択することで、weko\_gridlayout.admin.WidgetSettingView.action\_deleteが呼び出され、db内のfacet\_search\_settingテーブルから選択した情報が削除される。

<!-- end list -->

  - > 更新履歴

<table>
<thead>
<tr class="header">
<th>日付</th>
<th>GitHubコミットID</th>
<th>更新内容</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>2023/08/31</p>
</blockquote></td>
<td>353ba1deb094af5056a58bb40f07596b8e95a562</td>
<td>初版作成</td>
</tr>
</tbody>
</table>