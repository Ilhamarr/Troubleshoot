# Documentation




### C. Sturture of my source code

##### Directory

1. all of java file is in directory
app >> Java >> com.latihan.troubleshoot.id
--> **MainActivity** is a core for run this program. all component must be call in here
--> **historyfragment**,**historyfragment**,**profilefragment** is a fragment menu from bottom navigation. execution what doing in the fragment, code in that class.
--> **SignUp** & **Login** syntax to log in into homefragment
--> **splashscreen** is view when the first time open the app.

2. all rhe resouce (Asset, layouting, color etc.) are in:
app >> res
--> all of the template or view are in **layout** directory
--> all of the asset (picture or vektor) are in **drawable** directory
--> for setting the view of fragment, this is need a new file resource, this is in *menu directory*
--> for setting to add color and style for component, its can edit in **value** directory.

##### function 
this a explain of function that i use.

```sh
public class MainActivity extends AppCompatActivity implements View.OnClickListener {
```
this function explan the main activity implementing the cliking the item.

```sh
  protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_sign_up2);
        BottomNavigationView bottomNav = findViewById(R.id.bottomNavigation);
        bottomNav.setOnNavigationItemSelectedListener(navListener);
```
this is a declare the target layout and id.
layout == using 'view'
button, text == using 'id'

```sh
   private BottomNavigationView.OnNavigationItemSelectedListener navListener = new BottomNavigationView.OnNavigationItemSelectedListener() {
        @Override
        public boolean onNavigationItemSelected(@NonNull MenuItem Item) {
            Fragment selectedFragment = null;
            switch (Item.getItemId()) {
                case R.id.nav_home:
                    selectedFragment = new homefragment();
                    break;
                case R.id.nav_history:
                    selectedFragment = new historyfragment();
                    break;
                case R.id.nav_profile:
                    selectedFragment = new profilefragment();
                    break;
            }
            getSupportFragmentManager().beginTransaction().replace(R.id.fargment_container,
                    selectedFragment).commit();

            return true;
```

this is to call the fragment.

### D. Statistic

The total i write the code are 748 lines



