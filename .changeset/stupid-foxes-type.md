---
'@backstage/plugin-catalog-react': patch
---

Use the history API directly in `useEntityListProvider`.

This replaces `useSearchParams`/`useNavigate`, since I found that they caused additional rerenders.

Table re-render count is down additionally:

- Initial render of catalog page: 12 -> 9
- Full `CatalogPage` test: 57 -> 48
