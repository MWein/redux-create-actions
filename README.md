# redux-create-actions
Functions for creating actions for use with redux

The createActions function returns an object of constants and actions given a namespace and an object with desired action names.

const actionBundle = createActions('app', {
  setPage: 'SET_PAGE',
})

This function returns the following object.

{
  constants: {
    SET_PAGE: '@app/SET_PAGE',
  },
  actions: {
    setPage: [Redux Function]
  }
}

The redux function, setPage('The Payload'), will return { type: '@app/SET_PAGE', payload: 'The Payload' }
