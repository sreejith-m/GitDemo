# GitDemo

1) In forminit() or formeditinit()

this.minDate = new Date();
        this.minDate.setDate(this.minDate.getDate() + 1);
        // set enddate mindate
        this.addProjectForm.get('startDateControl').valueChanges.subscribe(val => {
            this.addProjectForm.controls.endDateControl.reset();
            this.minDate = val;
            this.minDate.setDate(this.minDate.getDate() + 1);
        });
        
        
 2) webconfig
 
 <configuration>
<system.webServer>
  <rewrite>
    <rules>
      <rule name="Angular Routes" stopProcessing="true">
        <match url=".*" />
	  <conditions logicalGrouping="MatchAll">
	    <add input="{REQUEST_FILENAME}" matchType="IsFile" negate="true" />
	    <add input="{REQUEST_FILENAME}" matchType="IsDirectory" negate="true" />
	  </conditions>
	  <action type="Rewrite" url="/" />
	  <!--<action type="Rewrite" url="/" />-->
      </rule>
    </rules>
  </rewrite>
</system.webServer>
</configuration>
