# Demo

https://leekevinyg.github.io/react-tag-input/.

# React Tag Input 

A simple (but fully customizable) react tag input component built using styled components.

To start up a dev env that runs the example react app utilizing the component: 

* ``` npm install ``` 
* ``` npm start ```

To build the example app: 

* ``` npm run build-examples ``` 

The output of the above command is what is running at https://leekevinyg.github.io/react-tag-input/.

To build for an npm registry: 

* ``` npm run build ```. 

When this command is run, contents in the ```src/lib``` will be bundled and outputted to the ```dist``` folder. This folder can then be deployed to an npm registry of your choice.

# Component Interface

This component exposes the following props to allow for customization:

* **wrapperStyle**

A js template string to be used to override the default component wrapper styles. The example below will override the wrapper ```background``` and disable the default ```box-shadow```. The template string can be anything that you would normally pass down as a [styled-component](https://www.styled-components.com/docs/basics#getting-started "Styled Component") configuration.

```
  <TagInput wrapperStyle={`
    background: red;
    box-shadow: none;
  `}/>

```

* **inputStyle**

A js template string to be used to override the default component input styles. The example below will override the input ```background``` color and override the placeholder text styling in webkit based browsers. The template string can be anything that you would normally pass down as a [styled-component](https://www.styled-components.com/docs/basics#getting-started "Styled Component") configuration.

```
  <TagInput inputStyle={`
    background: red;
    &::-webkit-input-placeholder {
      font-weight: 600;
      font-style: bold;
      color: black;
    }
  `}/>

```

* **tagStyle**

A js template string to be used to override the default component tag styles. The example below will override the tag ```background``` color. The template string can be anything that you would normally pass down as a [styled-component](https://www.styled-components.com/docs/basics#getting-started "Styled Component") configuration.

```
  <TagInput tagStyle={`
    background: red;
  `}/>

```

* **addTagOnEnterKeyPress**

A boolean flag to control whether hitting the enter will will add a tag into the input. Defaults to true.

```
  <TagInput addTagOnEnterKeyPress={false} />

```