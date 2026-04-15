# React Tabs with Router

Implement the `App` with `Home` page available at `/` and `Tabs` page available
at `/tabs`. Each page should have the correct title `Home page` or `Tabs page`.
The `Tabs` page should also show a `Tabs` component implemented in [React Tabs JS](https://github.com/mate-academy/react_tabs-js#react-tabs-js)
or [React Tabs](https://github.com/mate-academy/react_tabs#react-tabs).

> Here is [the working version](https://mate-academy.github.io/react_tabs-with-router)

1. Navigation with `Home` and `Tabs` links:
    - should be visible on every page;
    - should highlight an active link with `is-active` class;
1. `TabsPage` page should work for both `/tabs` and `/tabs/:tabId` paths (use nested routes);
    ```tsx
    <Route path="tabs">
      <Route index element={<TabsPage />} />
      <Route path=":tabId" element={<TabsPage />} />
    </Route>
    ```
1. Each tab should update the URL on click.
    - the URL should follow the next format `/tabs/:tabId` (use actual `tab.id` instead of `:tabId`);
    - replace `<a href="#...">` with `<Link to="/tabs/...">` and remove `onClick`;
    - **don't** use `NavLink` as `is-active` class is added to a parent element;
    - read `tabId` from the URL using [useParams](https://reactrouter.com/en/main/hooks/use-params) hook;
    - if the `tabId` does not match any tab show `Please select a tab` message instead of a tab content.
1. The page should show the same content after a reload.
1. Redirect from `/home` to `/` using the [Navigate](https://reactrouter.com/en/main/components/navigate) component;
1. Show the `Page not found` title for all the other URLs;

## Instructions
- Install Prettier Extention and use this [VSCode settings](https://mate-academy.github.io/fe-program/tools/vscode/settings.json) to enable format on save.
- Implement a solution following the [React task guideline](https://github.com/mate-academy/react_task-guideline#react-tasks-guideline).
- Use the [React TypeScript cheat sheet](https://mate-academy.github.io/fe-program/js/extra/react-typescript).
- Open one more terminal and run tests with `npm test` to ensure your solution is correct.
- Replace `<your_account>` with your Github username in the [DEMO LINK](https://NemH.github.io/react_tabs-with-router/) and add it to the PR description.

Реалізуйте `App` зі сторінкою `Home`, доступною за адресою `/`, та сторінкою `Tabs`, доступною
за адресою `/tabs`. Кожна сторінка повинна мати правильну назву `Home page` або `Tabs page`.
Сторінка `Tabs` також повинна відображати компонент `Tabs`, реалізований у [React Tabs JS](https://github.com/mate-academy/react_tabs-js#react-tabs-js)
або [React Tabs](https://github.com/mate-academy/react_tabs#react-tabs).

> Ось [робоча версія](https://mate-academy.github.io/react_tabs-with-router)

1. Навігація за допомогою посилань `Home` та `Tabs`:
- має бути видимою на кожній сторінці;
- має виділяти активне посилання за допомогою класу `is-active`;
1. Сторінка `TabsPage` має працювати як для шляхів `/tabs`, так і для `/tabs/:tabId` (використовуйте вкладені маршрути);
```tsx
<Route path="tabs">
<Route index element={<TabsPage />} />
<Route path=":tabId" element={<TabsPage />} />
</Route>
```
1. Кожна вкладка повинна оновлювати URL-адресу при кліку.
- URL-адреса повинна мати такий формат `/tabs/:tabId` (використовуйте фактичний `tab.id` замість `:tabId`);
- замініть `<a href="#...">` на `<Link to="/tabs/...">` та видаліть `onClick`;
- **не** використовуйте `NavLink`, оскільки клас `is-active` додається до батьківського елемента;
- зчитати `tabId` з URL-адреси за допомогою хука [useParams](https://reactrouter.com/en/main/hooks/use-params);
- якщо `tabId` не відповідає жодній вкладці, показати повідомлення `Buy ласка, виберіть вкладку` замість вмісту вкладки.
1. Сторінка повинна відображати той самий вміст після перезавантаження.
1. Перенаправити з `/home` на `/` за допомогою компонента [Navigate](https://reactrouter.com/en/main/components/navigate);
1. Показувати заголовок `Сторінку не знайдено` для всіх інших URL-адрес;
