# Shadcn UI installation with correct configurations in NEXT JS 13

## Correct way of installation:

First of all create a new project of **NEXT JS 13** with standard configurations

    `npx create-next-app@latest project-name`

Try using these configurations:

```shell
√ Would you like to use TypeScript? ... No / Yes
√ Would you like to use ESLint? ... No / Yes
√ Would you like to use Tailwind CSS? ... No / Yes
√ Would you like to use `src/` directory? ... No / Yes
√ Would you like to use App Router? (recommended) ... No / Yes
√ Would you like to customize the default import alias? ... No / Yes
```

Now install **Shadcn UI** using command given following:

    `npx shadcn-ui@latest init`

And use the following configuration for **Shadcn ui** if you used the above given **NEXT JS 13** configurations:

```shell
√ Which style would you like to use? » Default
√ Which color would you like to use as base color? » Slate
√ Where is your global CSS file? ... src/app/globals.css
√ Do you want to use CSS variables for colors? ... no / `yes`
√ Where is your tailwind.config.js located? ... tailwind.config.js
√ Configure the import alias for components: ... @/components
√ Configure the import alias for utils: ... @/lib/utils
√ Are you using React Server Components? ... no / `yes`
√ Write configuration to components.json. Proceed? ... `yes`
```

**NOTE:** One main thing to notice here which is the root cause of the errors is **_wrong placing of_** **globals.css** file just make sure you have added the path as:

    `src/app/globals.css`

## Incorrect way of installation and errors:

**Next js 13** Project is created along with the standard configurations **_as given above._**

But at the time of installation of shadcn ui the configuration is used is 👇🏻:
![Shadcn wrong configuration](https://github.com/AbuHurairah127/Shadcn-ui-with-Nextjs-13/blob/main/images/Shadcn%20intallation.PNG)
