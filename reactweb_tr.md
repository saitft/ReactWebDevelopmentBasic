# ReactWebDevelopmentBasic
React ile nasıl Web geliştirilir ilk adımlar nelerdir?

React ile web geliştirmek için aşağıdaki adımları takip edebilirsiniz:

1. React Kurulumu: İlk olarak, React'i projenize eklemeniz gerekiyor. React'i kullanabilmek için Node.js yüklü olmalı ve bir paket yöneticisi olan npm veya Yarn kullanmalısınız. Ardından, bir React projesi oluşturmak için aşağıdaki komutları kullanabilirsiniz:

```shell
npx create-react-app proje-adı
```

Bu komut, projenizin temel bir yapılandırmasını oluşturur ve gerekli bağımlılıkları indirir.

2. React Component'leri: React, bileşen tabanlı bir yaklaşım kullanır. Bu nedenle, web arayüzünüzü oluşturmak için bileşenler oluşturmanız gerekmektedir. Her bileşen, kendi içindeki durumu (state) yönetebilir ve JSX syntax'ını kullanarak görüntülenecek HTML yapılarını tanımlayabilir. Örneğin, aşağıdaki gibi bir bileşen oluşturabilirsiniz:

```javascript
import React from 'react';

class App extends React.Component {
  render() {
    return (
      <div>
        <h1>Merhaba, Dünya!</h1>
      </div>
    );
  }
}

export default App;
```

3. Bileşenlerin Kullanımı: Oluşturduğunuz bileşenleri diğer bileşenlerde veya ana uygulama bileşeninde kullanabilirsiniz. Örneğin, ana bileşen (App) içinde diğer bileşenleri çağırabilir ve düzenleyebilirsiniz:

```javascript
import React from 'react';
import Header from './Header';
import Content from './Content';
import Footer from './Footer';

class App extends React.Component {
  render() {
    return (
      <div>
        <Header />
        <Content />
        <Footer />
      </div>
    );
  }
}

export default App;
```

4. React JSX ve Props: JSX, JavaScript ile HTML'i birleştiren bir syntax'tır. JSX kullanarak bileşenlerin görüntülenecek HTML yapısını tanımlayabilirsiniz. Props ise bileşenlere parametre olarak geçilebilecek verilerdir. Örneğin:

```javascript
import React from 'react';

class Greeting extends React.Component {
  render() {
    return <h1>Merhaba, {this.props.name}!</h1>;
  }
}

export default Greeting;
```

Kullanımı:

```javascript
import React from 'react';
import Greeting from './Greeting';

class App extends React.Component {
  render() {
    return (
      <div>
        <Greeting name="Ahmet" />
        <Greeting name="Mehmet" />
      </div>
    );
  }
}

export default App;
```

5. React State Yönetimi: React, bileşenlerin içindeki durumu (state) yönetmek için bir mekanizma sunar. Bileşenin durumu değiştiğinde, React otomatik olarak ilgili bileşenin sadece değişen kısımlarını gü

nceller. Durum yönetimi için `setState()` yöntemini kullanabilirsiniz. Örneğin:

```javascript
import React from 'react';

class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  increment() {
    this.setState({ count: this.state.count + 1 });
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={() => this.increment()}>Artır</button>
      </div>
    );
  }
}

export default Counter;
```

6. React Router (İsteğe Bağlı): React Router, web uygulamalarında gezinme (routing) işlemlerini yönetmek için kullanılan bir kütüphanedir. Birden fazla sayfa veya rotaya sahip uygulamaları geliştirmek için React Router'ı kullanabilirsiniz. React Router'ı projenize dahil etmek için aşağıdaki gibi bir komut kullanabilirsiniz:

```shell
npm install react-router-dom
```

React Router'ın kullanımı için ayrıntılı belgelere başvurabilirsiniz.

Bu adımları takip ederek React ile web geliştirmeye başlayabilirsiniz. React, daha karmaşık ve ölçeklenebilir web uygulamaları geliştirmek için geniş bir ekosisteme sahiptir, bu nedenle ihtiyaçlarınıza uygun diğer kütüphane ve araçları da keşfedebilirsiniz.
