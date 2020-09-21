# Flutter Extended Live Templates For Android Studio

Collection of my personal live templates for Flutter, BLoC, freezed or LogX library.

For using in your Android Studio see this [StackOverflow answer](https://stackoverflow.com/a/44177549).

- [Flutter Extended Live Templates For Android Studio](#flutter-extended-live-templates-for-android-studio)
  - [Flutter](#flutter)
    - [`cc`: const constructor](#cc-const-constructor)
    - [`gaph`: horizontal SizedBox](#gaph-horizontal-sizedbox)
    - [`gapv`: vertical SizedBox](#gapv-vertical-sizedbox)
    - [`printx`: extended `print`](#printx-extended-print)
    - [`st`: setState](#st-setstate)
  - [BLoC](#bloc)
    - [`blb`: BlocBuilder](#blb-blocbuilder)
    - [`cstless`: const StatelessWidget](#cstless-const-statelesswidget)
    - [`blc`: BlocConsumer](#blc-blocconsumer)
    - [`blimport`: BLoC import](#blimport-bloc-import)
    - [`bll`: BlocListener](#bll-bloclistener)
    - [`bloc`: BLoC](#bloc-bloc)
    - [`cubit`: Cubit](#cubit-cubit)
  - [freezed](#freezed)
    - [`cf`: const factory constructor](#cf-const-factory-constructor)
    - [`cpf`: const public factory constructor](#cpf-const-public-factory-constructor)
    - [`fimport`: freezed import](#fimport-freezed-import)
    - [`funion`: freezed union](#funion-freezed-union)
  - [LogX](#logx)
    - [`logx`: static LogX log](#logx-static-logx-log)

## Flutter

### `cc`: const constructor

```
const $class$($END$);
```

### `gaph`: horizontal SizedBox

```
const SizedBox(width: $width$)$END$
```

### `gapv`: vertical SizedBox

```
const SizedBox(height: $height$)$END$
```

### `printx`: extended `print`

Automatically fills in class and method name of current context.

```
print('[$name$] $END$');
```

### `st`: setState

Use *Surround With* functionality in Android Studio to wrap currently selected text with `setState`.

```
setState(() {
  $SELECTION$
});
```

## BLoC

### `blb`: BlocBuilder

```
BlocBuilder<$bloc$, $state$>(
    builder: (context, state) {
        $END$
    },
)
```

### `cstless`: const StatelessWidget

```
class $NAME$ extends StatelessWidget {
  const $NAME$();
  
  @override
  Widget build(BuildContext context) {
    return $END$;
  }
}
```

### `blc`: BlocConsumer

```
BlocConsumer<$bloc$, $state$>(
    listener: (context, state) {
    
    },
    builder:  lightTheme(context, state) {
        $END$
    },
)
```

### `blimport`: BLoC import

```
import 'package:flutter_bloc/flutter_bloc.dart';
```

### `bll`: BlocListener

```
BlocListener<$bloc$, $state$>(
    listener: (context, state) {
        $END$
    },
)
```

### `bloc`: BLoC

```
import 'package:flutter_bloc/flutter_bloc.dart';

class $name$ extends Bloc<$event$, $state$> {
  $name$() : super($initialState$);

  @override
  Stream<$state$> mapEventToState($event$ event) async* {
    $END$
  }
}
```

### `cubit`: Cubit

```
import 'package:flutter_bloc/flutter_bloc.dart';

class $name$ extends Cubit<$state$> {
  $name$() : super($initialState$);

  $END$
}
```

## freezed

### `cf`: const factory constructor

```
const factory $class$.$name$($END$) = _$class$$nameCap$;
```

### `cpf`: const public factory constructor

```
const factory $class$.$name$($END$) = $class$$nameCap$;
```

### `fimport`: freezed import

```
import 'package:flutter/foundation.dart';
import 'package:freezed_annotation/freezed_annotation.dart';

part '$file$.freezed.dart';

$END$
```

### `funion`: freezed union

```
@freezed
abstract class $name$ with _$$$name$ {
  $END$
}
```

## LogX

### `logx`: static LogX log

Automatically fills in class and method name of current scope. Remember to import [logx package](https://pub.dev/packages/logx)

```
Log.d('$text$', name: '$name$');
```

