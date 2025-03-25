# インターネットコンピュータークラブ (IC-CLUB)

## プレゼンテーション  
[IC-CLUB プレゼンテーションを見る](https://www.canva.com/design/DAGCxGq-jw8/g15VJ9h4MGvkW-FIB7AyNQ/edit?utm_content=DAGCxGq-jw8&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## デモ動画  
[IC-CLUB デモ動画を見る](https://youtu.be/iS0McRWXObk)


## Video: https://youtu.be/z4vAa_jubRY?si=D1mCEYCsOVZdx48r

### 	▶️ Experience the Live Site by Clicking the Link Below
<br>
<div align="center">
  <table>
    <tr>
      <th>Deployed On</th>
      <th>URL</th>
    </tr>
    <tr>
      <td>ICP MAINNET</td>
      <td>https://h7t4t-tyaaa-aaaap-abqka-cai.icp0.io
      </td>
    </tr>
    <tr>
      <td>ICP CANDID UI</td>
      <td>https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=hkun6-sqaaa-aaaap-abqjq-cai
</td>
    </tr>
    </table>
</div>
<br><br>


# 💡紹介
IC CLUBは、投資管理の分野を革命的に変える先駆的なプラットフォームです。IC CLUBの核となるのは、分散型で迅速、かつ官僚主義から解放された環境を提供し、投資クラブの管理をユーザーに力強くサポートすることです。このプラットフォームは、透明性、安全性、効率性を確保するために革新的な技術を活用しています。

IC CLUBの特徴の1つは、分散型へのこだわりです。ブロックチェーン技術を活用することで、投資クラブのデータを透明で安全かつ改ざん不可能なものにします。この分散型アプローチにより仲介者の必要性が排除され、ユーザーが直接投資管理をコントロールできるようになります。

# 💡ビジョン
IC CLUBは、投資管理を分散化、自立性、革新性に根ざした未来の中核に織り込むことを目指しています。私たちのビジョンは、個人を力強くサポートし、財務的な自立を育み、透明性と安全性の基準を再定義することで、従来の投資クラブの枠組みを変革することです。

この未来において、IC CLUBは分散化の象徴となり、ブロックチェーン技術の力を活用して投資管理の新時代を切り開きます。ユーザーが官僚主義や仲介者の制約から解放され、自分の財務活動を直接コントロールできる世界を実現します。このプラットフォームは、透明性、安全性、効率性を追求し、ユーザーのニーズに応える柔軟で迅速な設計となっています。

# 何ができるのか

### 投資クラブの作成
- ユーザーはクラブ名を指定するだけで簡単に投資クラブを作成可能。
- 作成したクラブは、作成者のアカウント（オーナー）に関連付けられます。

### クラブへの参加・退出
- ICP（Internet Computer Protocol）ブロックチェーンアカウントを持つ人なら誰でも、利用可能な投資クラブに参加したり、数クリックで退出したりできます。

### クラブへの貢献
- メンバーは、ICPコインを寄付することで共通資金（プール）に貢献できます。
- 寄付金は提案で利用可能です。

### 提案の作成と投票
- クラブプールに資金を提供するメンバーは、提案を作成可能。
- 提案には説明、金額（プール金額を超えない）、および投資先が含まれます。
- 全メンバーが各提案に対して1票の投票権を持ち、承認または却下を決定します。

### 提案の実行
- 提案が承認多数の場合、提案者は提案を実行可能。
- このアクションにより、指定された受取人に提案金額が送金されます。
- 提案者は、キャンセルや送金防止などの理由で提案を終了することもできます。

# 🔍解決する問題
IC CLUBは、従来のプライベート投資ファンド市場で直面していた体系的な課題に対応します。これにより、スタートアップを含む革新的なプロジェクトへの資金調達に参加したいと望む投資家が直面する障壁を取り除きます。

# 💥直面した課題

### MOTOKO:
スケーラブルなスマートコントラクトを構築することは、ハードな作業と献身が求められる困難な作業です。それにもかかわらず、私はそれを実現することができました。主な課題は、すべてのユーザーに対して動的かつ柔軟に対応できるコントラクトを作成することでした。例えば、ユーザーがコースを追加した場合、それはそのユーザーのダッシュボードにのみ表示され、他のログインしたユーザーには表示されないようにする必要がありました。


## Code explanation 

# クラブスマートコントラクト概要

このコードは、インターネットコンピュータプラットフォーム上でMotokoを使用して、金融クラブを管理するためのスマートコントラクトを表しています。このコントラクトは、クラブ管理、提案、投票、およびメンバーとのやり取りの機能を含みます。

## 機能

### 認証
- **`whoami`**: 呼び出し元のプリンシパルを返し、認証を行います。

### クラブ管理
- **ClubInfo タイプ**: クラブの詳細を含む `title` と `description` を保持します。
- **createClub**: ユニークなIDで新しいクラブを作成します。
- **GetClub**: IDによってクラブの詳細を取得します。

### 提案管理
- **Proposol タイプ**: `title`、`description`、`destination`、`Amount`、`password` を含む提案の詳細を保持します。
- **createProposal**: ユニークなIDで新しい提案を追加します。
- **GetProposol**: IDによって提案を取得します。

### 投票機能
- **YesVote**: 「賛成」票のカウントを増やします。
- **NOVote**: 「反対」票のカウントを増やします。
- **GetYesVote**: 合計の「賛成」票を取得します。
- **GetNoVote**: 合計の「反対」票を取得します。

### カウンターと残高
- **SetProposalCount** と **GetProposalCount**: 提案のカウントを管理および取得します。
- **SetMemberCount** と **GetMemberCount**: メンバーのカウントを管理および取得します。
- **SetBalance** と **GetBalance**: クラブの残高を更新および取得します。

### ステータス管理
- **SetStatus**: 指定されたIDのステータスを設定します。
- **GetStatus**: 指定されたIDのステータスを取得します。

### ユーティリティ
- **ClubId**: 現在のクラブIDカウントを返します。
- **ProposalId**: 現在の提案IDカウントを返します。

## データストレージ
- `HashMap` を使用して、クラブ、提案、およびステータスを保存します。
- ステーブル変数は、アップグレード間で永続的なストレージを確保します。

## 主な変数
- `postIdCount`: クラブIDを追跡します。
- `proposolIdCount`: 提案IDを追跡します。
- `YesVoteCount` と `NoVoteCount`: 投票数を追跡します。
- `ProposalCount`、`MemberCount`、`Balance`: クラブ全体の指標を管理します。
