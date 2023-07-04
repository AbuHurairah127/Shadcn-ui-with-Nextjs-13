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

After successful installation of next js and shadcn ui Project folder structure will look like:

![Shadcn wrong configuration](https://github.com/AbuHurairah127/Shadcn-ui-with-Nextjs-13/blob/main/images/correct%20folder%20structure.PNG)

and components.json file will look like:

![Shadcn wrong configuration](https://github.com/AbuHurairah127/Shadcn-ui-with-Nextjs-13/blob/main/images/Shadcn%20intallation%20correct%20component.png)

## Incorrect way of installation and errors:

**Next js 13** Project is created along with the standard configurations **_as given above._**

But at the time of installation of shadcn ui the configuration is used is 👇🏻:

![Shadcn wrong configuration](https://github.com/AbuHurairah127/Shadcn-ui-with-Nextjs-13/blob/main/images/Shadcn%20intallation.PNG)

**Note:** The main wrong configuration used here is **_wrong placing of globals.css file_**:

    `app/globals.css`

After the configurations you will get the folder structure same as given below:

![Shadcn wrong configuration](https://github.com/AbuHurairah127/Shadcn-ui-with-Nextjs-13/blob/main/images/Folder%20Structure%20with%20wrong%20config.PNG)

And the `components.json` file will be like:

![Shadcn wrong configuration](https://github.com/AbuHurairah127/Shadcn-ui-with-Nextjs-13/blob/main/images/Shadcn%20intallation%20wrong%20component.json.PNG)

### ERROR EXPLANATION

- First the project is created and started next js server.
- The next js compiler will read all of your code and will get only one `app` directory in the `src` directory.
- Now the Shadcn ui Library is intalled with **wrong configuration** and the next js server is still running will not take care of the new `app` directory at the root.
- But once the next js compiler is turned of and started again it will check all the code again and this time it will **ignore** the `app` directory present in `src` directory.
- Now an error will be received `404|Page not found`. Now you might have noticed that the `app` directory at root has only globals.css file no `page.tsx` file. Means that your application has no page.Thus, it causes an error.

#### Best of luck for your next project! Stay Blessed.
