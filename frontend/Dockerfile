# 軽量なnode.js環境（Alpin LINUXベース）をベースに使用
FROM node:18-alpine 
# 作業ディレクトリを/appに設定。
WORKDIR /app
# 依存関係ファイルを（パッケージ情報）をコンテナにコピー
# Next.jsを含む依存パッケージをインストール
COPY package.json package-lock.json ./
RUN npm install
# 残りのファイル（ソースコードなど）をコンテナにコピー。
COPY . .
# コンテナの3000ポートを外部に公開（開発用ポート）。
EXPOSE 3000
# デフォルト起動コマンドとしてNext.jsの開発サーバーを実行。
CMD ["npm", "run", "dev"]