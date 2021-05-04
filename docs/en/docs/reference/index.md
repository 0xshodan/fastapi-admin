# Configuration

The following configurations can be used to `admin_app.configure(...)`.

## logo_url

Will show the logo image in admin dashboard.

## login_logo_url

Will show the logo in login page.

## admin_path

Default is `/admin`, but you can change to other page.

## maintenance (💗 Pro only)

If set to `true`, all pages will be redirected to the `/maintenance` page.

## redis

Instance of `aioredis`.

## default_locale

Current support `zh` and `en`, default is `en`.

## template_folders

Template folders registered to jinja2 and also can be used to override builtin templates.

## login_provider

You can pass subclasses of `fastapi_admin.providers.login.LoginProvider`, there is a
builtin `fastapi_admin.providers.login.UsernamePasswordProvider` you can use.

### admin_model

Subclass instance of `fastapi_admin.models.AbstractAdmin`.

### enable_captcha (💗 Pro only)

Show captcha in admin login page.

## permission_provider (💗 Pro only)

You can enable permission control by setting `permission_provider`, which is instance
of `fastapi_admin.providers.permission.PermissionProvider` of its subclass.

### admin_model

Subclass of `fastapi_admin.models.AbstractAdmin`.

### resource_model

Subclass of `fastapi_admin.models.AbstractResource`.

### permission_model

Subclass of `fastapi_admin.models.AbstractPermission`.

## admin_log_provider

You can enable action log by set `admin_log_provider`, which is instance
of `fastapi_admin.providers.admin_log.AdminLogProvider` or its subclass. After set that, all `delete/create/update` for
model will be recorded.

## search_provider  (💗 Pro only)

You can enable global search by setting `search_provider`, which is instance
of `fastapi_admin.providers.search.SearchProvider`, and then will display a search input in all pages.
