Uppgift 2- WebView
Nedan så visas en bit kod för hur en WebView gjordes. Den fick ett Id, sedan fick den mått som den skulle förhålla sig till, i detta fall så var både bredden och höjden “wrap_content” men även förhålla sig till sin parent node. 
<WebView
   android:id="@+id/nystring"
   android:layout_width="wrap_content"
   android:layout_height="wrap_content"
   android:text="@string/nystring"
   app:layout_constraintBottom_toBottomOf="parent"
   app:layout_constraintEnd_toEndOf="parent"
   app:layout_constraintStart_toStartOf="parent"
   app:layout_constraintTop_toBottomOf="@+id/appBarLayout"
   />

Här visas hur en extern webbplats och intern Webview visas i applikationen. På höger sida är den externa och på vänster den interna. 



 För att de ska visas när menyn klickas så används denna kod. Vad som visas nedan är kod för extern och intern webbapplikation. 

   @Override
   public boolean onOptionsItemSelected(MenuItem item) {
            int id = item.getItemId();

          if (id == R.id.action_external_web) {
           showExternalWebPage();
           Log.d("==>","Will display external web page");
           return true;
       }

       if (id == R.id.action_internal_web) {
           showInternalWebPage();
           Log.d("==>","Will display internal web page");
           return true;
       }

       return super.onOptionsItemSelected(item);
   }
}




