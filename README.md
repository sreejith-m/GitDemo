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
