# AngularDragStepper || <a href="https://abpprkonsalting.github.io/angular-drag-stepper/" rel="nofollow">Demo</a>


General description
=======================


A variant of material stepper component designed for been controlled by dragging the steps sideways. It's suited to work out of the box in both directions, horizontally and vertically. The later in xs layout, but that can be adjusted.


Exports the class "DragStepperComponent" as component ready to use using the selector <drag-stepper></drag-stepper>

Inside the component goes the steps as <cdk-step></cdk-step>


```

<drag-stepper>

  <cdk-step> step 1 template </cdk-step>

  <cdk-step> step 2 template </cdk-step>

  <cdk-step> step 3 template </cdk-step>

</drag-stepper>

```


Export an injectable that can be imported by any other component in the application for sending controlling commands (next, prev, or an especific step number to go to).

For example, from an internal component in an specific step:


```

export class Step1Component {

  constructor(protected stepperMessagesHandle: DragStepperMessagesHandle<Partial<any>>) {}


  onCardClick(){
    this.stepperMessagesHandle.next({value:"next"});
  }

  gotoFive() {
    this.stepperMessagesHandle.next({value:5});
  }

}


```

