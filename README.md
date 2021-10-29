# multi-step-form-handler

> Made with create-react-library

[![NPM](https://img.shields.io/npm/v/multi-step-form-handler.svg)](https://www.npmjs.com/package/multi-step-form-handler) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save multi-step-form-handler
```

## Usage

### Example form

```tsx
function FormA({ handleOnChange, errors, values }) {
  return (
    <form>
      <input
        type='text'
        name='name'
        onChange={handleOnChange}
        value={values.name}
      />
      {errors.name ? <p>{errors.name}</p> : null}
    </form>
  )
}
```

```tsx
import * as React from 'react'
import FormHandler, {useForm, useForm} from 'multi-step-form-handler'
import {FormA, FormB, FormC} from './forms'
import Button from './button'


function Example(){
    return (
      <FormHandler
        initialValues={initialValues}
        validationSchema={schema}
      >{({nextPage, previousPage, onSubmit, currentPage})} =>{
        return(
          <h2>{currentPage}</h2>
        <FormHandler.Forms>
          <FormA />
          <FormB />
          <FormC />
        </FormHandler.Forms>
        <FormHandler.Buttons>
          <Button onClick={previousPage}>Previous</Button>
          <Button onClick={nextPage}>Next</Button>
        </FormHandler.Buttons>
        <Button onClick={onSubmit}>Submit</Button>
        )
      }

      </FormHandler.Forms>
    )

}
```

## License

MIT © [chekwas88](https://github.com/chekwas88)
