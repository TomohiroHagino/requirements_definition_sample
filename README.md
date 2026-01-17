# （公開用サンプル）Management ドキュメント

本ドキュメントは **公開用サンプル** です。  
記載している **画面名 / 機能名 / パス / URL / 構成 / 並び順** はすべて架空のもの（匿名化・改変済み）であり、実案件の内容と一致しません。  
ただし、「要件定義〜画面設計〜基本設計を整理するための作り方（ドキュメント構造）」は、実務で使用する形式にしています。

## 要件定義（Requirements）

- 事業概要
  - [ /public-spec/requirements/ ](/public-spec/requirements/)

- 稼働・記録 機能要件
  - [ /public-spec/requirements/20_activity_requirements.md ](/public-spec/requirements/20_activity_requirements.md)

- 申請・承認 機能要件
  - [ /public-spec/requirements/30_request_requirements.md ](/public-spec/requirements/30_request_requirements.md)

- 成果物・帳票 機能要件
  - [ /public-spec/requirements/40_output_requirements.md ](/public-spec/requirements/40_output_requirements.md)

- 共通機能要件
  - [ /public-spec/requirements/50_common_requirements.md ](/public-spec/requirements/50_common_requirements.md)

- 非機能要件
  - [ /public-spec/requirements/60_non_functional.md ](/public-spec/requirements/60_non_functional.md)

---

## 画面設計（Screen Design）

各画面フォルダ配下の `page.md` には、以下を含める想定です。
（作成途中のものは画像のみ出来上がった状態でどんどんアップしていく）

- 画面概要（目的 / 対象ユーザー / 前提）
- 画面構成（エリア / コンポーネント）
- フローチャート
- 入力項目（name, type, 必須, バリデーション, 例）
- 表示項目（一覧カラム / 詳細項目）
- 操作（ボタン / 遷移 / ダイアログ）
- 状態（下書き / 申請中 / 差し戻し / 承認 / 確定）
- 権限（閲覧可 / 編集可 / 実行可）
- エラー（表示方針 / 文言例）
- API（エンドポイント / リクエスト / レスポンス）
- ログ（監査ログ対象 / 記録内容）
- 備考（運用ルール / 例外）
- テストケース

### 利用者側（20_member）

#### ポータル（00_portal）

- [ /public-spec/basic_design/20_member/00_portal/page.md ](/public-spec/basic_design/20_member/00_portal/page.md)

#### 稼働・記録（10_activity）

- 日次入力
  - [ /public-spec/basic_design/20_member/10_activity/daily/[date]/page.md ](/public-spec/basic_design/20_member/10_activity/daily/[date]/page.md)
- 期間サマリー
  - [ /public-spec/basic_design/20_member/10_activity/summary/[period]/page.md ](/public-spec/basic_design/20_member/10_activity/summary/[period]/page.md)
- 変更申請
  - [ /public-spec/basic_design/20_member/10_activity/revisions/new/page.md ](/public-spec/basic_design/20_member/10_activity/revisions/new/page.md)
- 休み申請
  - [ /public-spec/basic_design/20_member/10_activity/leave/new/page.md ](/public-spec/basic_design/20_member/10_activity/leave/new/page.md)

#### 申請（20_requests）

- 申請一覧
  - [ /public-spec/basic_design/20_member/20_requests/claims/page.md ](/public-spec/basic_design/20_member/20_requests/claims/page.md)
- 申請詳細
  - [ /public-spec/basic_design/20_member/20_requests/claims/[claim_id]/page.md ](/public-spec/basic_design/20_member/20_requests/claims/[claim_id]/page.md)
- 明細（複数行）
  - [ /public-spec/basic_design/20_member/20_requests/claims/[claim_id]/line_items/page.md ](/public-spec/basic_design/20_member/20_requests/claims/[claim_id]/line_items/page.md)
- 添付
  - [ /public-spec/basic_design/20_member/20_requests/claims/[claim_id]/attachments/page.md ](/public-spec/basic_design/20_member/20_requests/claims/[claim_id]/attachments/page.md)

#### 成果物（30_outputs）

- 成果物一覧（画像のみ）
  - [ /public-spec/basic_design/20_member/30_outputs/exports/_img/exports_list.png ](/public-spec/basic_design/20_member/30_outputs/exports/_img/exports_list.png)
- 成果物明細（画像のみ）
  - [ /public-spec/basic_design/20_member/30_outputs/exports/_img/exports_detail.png ](/public-spec/basic_design/20_member/30_outputs/exports/_img/exports_detail.png)
- その他成果物
  - レイアウト類似想定のため省略

#### その他（40_misc）

- 例外申請は既存フォームを流用する運用
  - [ /public-spec/basic_design/20_member/10_activity/leave/new/page.md ](/public-spec/basic_design/20_member/10_activity/leave/new/page.md)
- miscフォルダは現在空。追加ページは不要。

---

### 運用者側（30_ops）

#### 概要（00_overview）

- 運用トップ（画像のみ）
  - [ /public-spec/basic_design/30_ops/00_overview/_img/overview.png ](/public-spec/basic_design/30_ops/00_overview/_img/overview.png)

#### 稼働確定（10_closing）

- 日次確定（画像のみ）
  - [ /public-spec/basic_design/30_ops/10_closing/daily/_img/daily_close.png ](/public-spec/basic_design/30_ops/10_closing/daily/_img/daily_close.png)
- 期間確定（画像のみ）
  - [ /public-spec/basic_design/30_ops/10_closing/period/_img/period_close.png ](/public-spec/basic_design/30_ops/10_closing/period/_img/period_close.png)

#### 申請運用（20_review）

- 申請受信箱（画像のみ）
  - [ /public-spec/basic_design/30_ops/20_review/inbox/_img/inbox.png ](/public-spec/basic_design/30_ops/20_review/inbox/_img/inbox.png)
- 申請確認（画像のみ）
  - [ /public-spec/basic_design/30_ops/20_review/inbox/[id]/_img/review.png ](/public-spec/basic_design/30_ops/20_review/inbox/[id]/_img/review.png)
- 集計（画像のみ）
  - [ /public-spec/basic_design/30_ops/20_review/metrics/_img/metrics.png ](/public-spec/basic_design/30_ops/20_review/metrics/_img/metrics.png)
- 承認対応（画像のみ）
  - [ /public-spec/basic_design/30_ops/20_review/approvals/_img/approvals.png ](/public-spec/basic_design/30_ops/20_review/approvals/_img/approvals.png)

#### 成果物管理（30_outputs）

- 成果物確認（画像のみ）
  - [ /public-spec/basic_design/30_ops/30_outputs/verification/_img/verification.png ](/public-spec/basic_design/30_ops/30_outputs/verification/_img/verification.png)
- 確定済み成果物（画像のみ）
  - [ /public-spec/basic_design/30_ops/30_outputs/final/_img/final.png ](/public-spec/basic_design/30_ops/30_outputs/final/_img/final.png)

#### 共通設定（40_settings）

- 承認ルール設定（画像のみ）
  - [ /public-spec/basic_design/30_ops/40_settings/approval_rules/_img/approval_rules.png ](/public-spec/basic_design/30_ops/40_settings/approval_rules/_img/approval_rules.png)

...

```

