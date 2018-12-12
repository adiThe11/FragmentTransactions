# FragmentTransactions
List of methods to draw fragments



        //------- draws a fragment instead of the current one
        //------- Use it when you need the fragment hierarchy , so you can go back to the precedent fragment
        //------- Example: sigh in process with multiple screens
        public void addFragmentToBackStack(Fragment fragment) {
            FragmentManager fragmentManager = getSupportFragmentManager();
            FragmentTransaction fragmentTransaction = fragmentManager.beginTransaction();
            //------- R.id.container is the id of the layout in where you want to draw the fragment
            //------- it must be in the activity xml file
            fragmentTransaction.replace(R.id.container, fragment);
            fragmentTransaction.addToBackStack(null);
            fragmentTransaction.commit();
        }

      //------- draws a fragment instead of the current one
      //------- Use it when you don't need the fragment hierarchy
      //------- Example: opening fragments from activity's side menu or bottom navigation bar
      public void replaceFragment(Fragment fragment) {
          FragmentManager fragmentManager = getSupportFragmentManager();
          FragmentTransaction fragmentTransaction = fragmentManager.beginTransaction();
          //------- R.id.container is the id of the layout in where you want to draw the fragment
          //------- it must be in the activity xml file
          fragmentTransaction.replace(R.id.container, fragment);
          fragmentTransaction.commit();
      }
