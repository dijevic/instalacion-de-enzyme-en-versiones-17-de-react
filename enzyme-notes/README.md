# implementacion

## ejemplo de instalacion

// para usar ENZYME :
// P1. instalar tres dependencias:

```
npm install --legacy-peer-deps --save-dev @wojtekmaj/enzyme-adapter-react-17
npm install --save-dev enzyme
npm i enzyme-to-json
```

// P2. Add a setupTests.js:
crear un arhivo setupTests.js(por lo generaral el react-creat app crea uno por defecto, borrar configuracion que trae y agregar lo siguiente)

```
import Enzyme from 'enzyme';
import Adapter from '@wojtekmaj/enzyme-adapter-react-17';
import {createSerializer} from 'enzyme-to-json';

Enzyme.configure({ adapter: new Adapter() })
expect.addSnapshotSerializer(createSerializer({mode: 'deep'}));


```
