# Documentation


Troubleshoot.id is a business in computer service. in this time, i make a application mobile to making easier consument to order our services.

### A. Motivate
when i starting the business with my friends. many orders come by whatsapp to ordering a repair comuter/laptop. we had a discussion how to make some apps to make a easier cosument to order our service and it can be make a trust about out business.

on our way to build this app, we have a problem in time. we must split time to serve a consument, work a collage task, and build this apps.

### B. Project Duration
I start work this on June 2020 and still on progress

### C. Sturture of my source code
I focused on layout and templating for this apps, so i build on XML file and JAVA on android studio.
##### Directory
my work are on directory :
1. all of my java file is in directory
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



