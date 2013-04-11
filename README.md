cdi-unit 
========

Unit testing for CDI applications. Supports EasyMock for mocking dependencies.

See website for full details https://jglue.org/cdi-unit/

```java
class Starship {
 
  @Inject
  Engine engine; //We don't know the exact engine that this ship will have.
 
  void start() {
    engine.start();
  }
}

@RunWith(CdiRunner.class)
@AdditionalClasses(WarpDrive.class) // WarpDrive is available to use.
class TestStarship {
 
  @Inject
  Starship starship;
 
  @Test
  public void testStart() {
    starship.start(); // Going to warp!
  }
}

```


Copyright 2013 Bryn Cooke
 
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
 
        http://www.apache.org/licenses/LICENSE-2.0
 
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.