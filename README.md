Angular Performance tuning:

Before you start improving performnace:

- Make sure the architecture is clean and readable before you start perfomance tuning.
- Thumb rule is your performance enhancement never "infect" your app.
- Follow LIFT Principle for folder structure and files(Locate code quickly, indentify code at a glance, Flattest structure possible, Try to be Dry)

Investigating Performance problems:

- Console log time
- use performance tab in Dev Tools.
- Network Tab in Dev tools.
- Measure excution time.

we have to prioritize the performance issues.

Fixing perfomance problems:
- set budget for the bundle sizes, to ensure you are not getting too big bundle.
- Take a flattest fix which will improve the perfomance.
- Meta Reducers: for ensuring you design yor app for immuatability the Ngrx store can ensure you never mutate the store.
- Make onPush the default change detection strategy.

angular.json

"schematics" : {
"@schematics/angular:component":{
"styleext":"scss",
"changeDetection":"OnPush"
},

- For Run Time performance:
By performing change detection, we have to change from ChangeDetectionStrategy to OnPush. 
- whenever changes happen in the component, if it is default then total DOm tree will update. if we chnaged from default to onPush then we have to update manually.
-
