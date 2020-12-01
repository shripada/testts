1. Create a project with template typescript like so:
```
npx create-react-app testts
```

2. Once the project is set up, open it in VSCode:
```
cd testts
code . 
```
The project opens in VSCode.  and the package.json will look with these deps installed:

```
  "dependencies": {
    "@testing-library/jest-dom": "^5.11.4",
    "@testing-library/react": "^11.1.0",
    "@testing-library/user-event": "^12.1.10",
    "@types/jest": "^26.0.15",
    "@types/node": "^12.0.0",
    "@types/react": "^16.9.53",
    "@types/react-dom": "^16.9.8",
    "react": "^17.0.1",
    "react-dom": "^17.0.1",
    "react-scripts": "4.0.1",
    "typescript": "^4.0.3",
    "web-vitals": "^0.2.4"
  },
```

3. Now simply modify the tsconfig.json. We shall change 
```
"jsx": "react-jsx"   ==> "jsx" : "react" 
```
Save tsconfig.json.  Observe that the changes are saved.

4. Now close the **testts**  workspace and open again.  Voila!, observe that tsconfig is quickly re created and overwritten with defaults, and see that  the change we made:
```
"jsx": "react"
```
is reset back to the default:
```
"jsx": "react-jsx" 
```

**Note that, we have not run any other commands like yarn start, etc.  tsconfig.json is automatically getting overrwritten the moment project is closed and reopened!.**

**Also note that, if I delete node_modules  and then make changes to tsconfig.json, close and open project, VSCode does not overwrite the tsconfig.json**   