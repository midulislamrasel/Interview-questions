### Components
#### Step : 01
```php
php artisan make:component alert
```

#### Step:02
any View Blade File

```php
<html>
    <body>
      <x-alert type="info" message="This is error messages"/>
      <x-alert type="success" message="This is Success message Alert"/>
    </body>
</html>

```


#### Step: 03
app/View/Components/alert.php

```php
<div class="alert alert-{{$type}}" role="alert">
    {{$message}}
</div>
``` 

#### Step: 04
view/components/alert.php
```php
class alert extends Component
{
    public $type;
    public $message;
    public function __construct(string $type, string $message)
    {
        $this->type = $type;
        $this->message = $message;
    }



    public function render(): View|Closure|string
    {
        return view('components.alert');
    }
}
```

### or (NOT GOOD)
##### view/components/alert.php
type and message Blade file same name so shot hand
```php
public function __construct(public string $type, public string $message){

}
```
