# Change Log
All notable changes to this project will be documented in this file.
`IBAnimatable` adheres to [Semantic Versioning](http://semver.org/).

## Versions
### Next

#### API breaking changes
None

#### Enhancements
- New gradient `startPoint`: `.custom(startX, startY, endX, endY)`. [#380](https://github.com/IBAnimatable/IBAnimatable/pull/380)
- Introducing `borderType`, find all the information in the documentation [#389](https://github.com/IBAnimatable/IBAnimatable/pull/380)

#### Bugfixes

- Fix `slide(.out, *)` and `squeeze(.out, *)` translation coordinates [#379](https://github.com/IBAnimatable/IBAnimatable/issues/379)
- Fix `No such module IBAnimatable` when attempting to run the Playground [#251](https://github.com/IBAnimatable/IBAnimatable/issues/251)
- Fix custom presentation animations [#393](https://github.com/IBAnimatable/IBAnimatable/pull/393)
- Fix border state when trying to reset a valid border [#398](https://github.com/IBAnimatable/IBAnimatable/pull/398)
 
### [3.1.2](https://github.com/IBAnimatable/IBAnimatable/releases/tag/3.1.2)

#### API breaking changes
None

#### Enhancements
- Add support for corner and shadow on UICollectionViewCell.
[#368](https://github.com/IBAnimatable/IBAnimatable/pull/368)
- Use Swift Enum as key in our internal presentation and transition cache.
[#360](https://github.com/IBAnimatable/IBAnimatable/issues/360)

#### Bugfixes
- Fix initial `cornerSide` rendering issue.
[#367](https://github.com/IBAnimatable/IBAnimatable/pull/367)

### [3.1.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/3.1.1)

#### API breaking changes
None

#### Enhancements
None

#### Bugfixes

- Make `PresentationPresenterManager ` and `TransitionPresenterManager ` `shared` property public again. [#364](https://github.com/IBAnimatable/IBAnimatable/issues/364)

### [3.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/3.1)

#### API breaking changes
None

#### Enhancements
- Add `cornerSide` to `CornerDesignable` to support multiple sides for corner. [#356](https://github.com/IBAnimatable/IBAnimatable/issues/356)

#### Bugfixes
None

### [3.0.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/3.0.1)

#### API breaking changes
None

#### Enhancements
None

#### Bugfixes

- Fix `clipsToBounds` issue.  [#303](https://github.com/IBAnimatable/IBAnimatable/issues/303)
- Fix `keyboardTranslation` when presenting a custom controller

### [3.0](https://github.com/IBAnimatable/IBAnimatable/releases/tag/3.0)

IBAnimatable 3.0 is the major release to support Swift 3 🎉.

#### API breaking changes
- This version follows Swift 3 [API Design Guidelines](https://swift.org/documentation/api-design-guidelines/) and contains a lot of breaking changes from version 2.x. Please check out [IBAnimatable 3.0 Migration Guide](Documentation/IBAnimatable 3.0 Migration Guide.md) for more information about how to migrate your project to 3.0.

#### Enhancements
- Complete Swift 3 Compatibility [#221](https://github.com/IBAnimatable/IBAnimatable/issues/221)
- New Swift enum system [#218](https://github.com/IBAnimatable/IBAnimatable/issues/218)

#### Bugfixes
- Fix `borderSides` [#280](https://github.com/IBAnimatable/IBAnimatable/issues/280)
- Fix blur effect view [#302](https://github.com/IBAnimatable/IBAnimatable/issues/302)

All issues associated with this version can be found using this [filter](https://github.com/IBAnimatable/IBAnimatable/milestone/2?closed=1).

---
### [2.8.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.8.1)

#### API breaking changes
None

#### Enhancements
Upgrade to Swift 2.3

#### Bugfixes
None

---
### [2.7](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.7)

#### API breaking changes

- `AnimatableStackView` doesn't conform anymore to `BlurDesignable`
- `AnimatableScrollView` doesn't conform anymore to `BlurDesignable`

#### Enhancements

- Support for custom presentation, for more information, [read the documentation](Documentation/Presentations.md)
- Introducing [AnimatableActivityIndicatorView](Documentation/ActivityIndicators.md) to support custom activity indicator animations. Already supporting 31 animations! Take a look at at the [full list](Documentation/ActivityIndicators.md)

#### Bugfixes

- Fixed `cornerRadius` when used with a gradient [#268](https://github.com/IBAnimatable/IBAnimatable/issues/268)
- Remove previous vibrancy view when adding setting a new vibrancy. Previous bug: all the views was staying in the hierarchy [#277](https://github.com/IBAnimatable/IBAnimatable/issues/277)
- Fixed "Shadows not working with Mask type" issue [#267](https://github.com/IBAnimatable/IBAnimatable/issues/267)

---
### [2.6](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.6)

#### API breaking changes
None

#### Enhancements
Move to IBAnimatable organization [#235](https://github.com/IBAnimatable/IBAnimatable/issues/235)

#### Bugfixes
None

---
### [2.5](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.5)

#### API breaking changes
None

#### Enhancements

- Add `vibrancyBlurEffect` to `BlurDesignable`. Once specify the Vibrancy effect style, all subviews will apply this vibrancy effect [#245](https://github.com/IBAnimatable/IBAnimatable/pull/245)
- New animations: `ZoomInvertIn` and ``ZoomInvertOut` [#249](https://github.com/IBAnimatable/IBAnimatable/pull/249)

#### Bugfixes
None

---
### [2.4](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.4)

#### API breaking changes
None

#### Enhancements
- New designable properties for `UITextView`: placeholder text and color [#227](https://github.com/IBAnimatable/IBAnimatable/issues/227)
- Add `AnimatableSlider` [#228](https://github.com/IBAnimatable/IBAnimatable/pull/228)
- Add `AnimatableScrollView` [#232](https://github.com/IBAnimatable/IBAnimatable/pull/232)


#### Bugfixes
- Use `UIBezierPath` to mask `Circle`, which can fix a bug when uses Circle mask with `borderSide` [#234](https://github.com/IBAnimatable/IBAnimatable/pull/234)
- Fix a bug for `Polygon` mask when the `width` is longer than the `height`. [#234](https://github.com/IBAnimatable/IBAnimatable/pull/234)
- Fix a crash when the parameters number of `Wave` mask is not 3. [#234](https://github.com/IBAnimatable/IBAnimatable/pull/234)

---
### [2.3](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.3)
#### API breaking changes

- Change `PanFromLeft`, `PanFromRight`, `PanFromTop`, `PanFromBottom`, `PanHorizontally` and `PanVertically` to `Pan(Left)`, `Pan(Right)`, `Pan(Top)`, `Pan(Bottom)`, `Pan(Horizontal)` and `Pan(Vertical)` for `Pan` gesture transition controller. [#125](https://github.com/IBAnimatable/IBAnimatable/issues/125)
- Refactor `direction` to `fromDirection` for system transition animators.  Refactor `TransitionFromDirection` to `TransitionDirection`. [#206](https://github.com/IBAnimatable/IBAnimatable/pull/206)
- Refactor `Fade`, `FadeIn` and `FadeOut` to `Fade(direction: TransitionDirection)` in `TransitionAnimationType`. Use `Fade(In)` to replace `FadeIn` and use `Fade(Out) to replace `FadeOut`.[#209](https://github.com/IBAnimatable/IBAnimatable/pull/209)
- Remove `PresentFadeInSegue`, `PresentFadeInWithDismissInteractionSegue`, `PresentFadeOutSegue` and `PresentFadeOutWithDismissInteractionSegue`, use  `PresentFadeSegue` and `PresentFadeWithDismissInteractionSegue` instead. [#209](https://github.com/IBAnimatable/IBAnimatable/pull/209)
- Remove `degree` for `SystemRotate` since it only supports 90 degrees. [#210](https://github.com/IBAnimatable/IBAnimatable/pull/210)

#### Enhancements

- Add `ScreenEdgePanInteractiveAnimator` to support `ScreenEdgePan(Left)`, `ScreenEdgePan(Right)`, `ScreenEdgePan(Top)`, `ScreenEdgePan(Bottom)`, `ScreenEdgePan(Horizontal)` and `ScreenEdgePan(Vertical)` for `ScreenEdgePan` gesture transition controller. [#125](https://github.com/IBAnimatable/IBAnimatable/issues/125)
- Support multiple sides for border [#168](https://github.com/IBAnimatable/IBAnimatable/pull/168)
- Add `ExplodeAnimator` to support Explode transition animation. It supports parameters `Explode(xFactor, minAngle, maxAngle)`, if no specified, the default values are `Explode(10, -10, 10)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `FoldAnimator` to support Fold transition animation. It supports parameters `Explode(direction, nbFolds)`, if no specified, the default values are `Fold(Left, 2)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `PortalAnimator` to support Portal transition animation. It supports parameters `Portal(direction, zoomScale)`, if no specified, the default values are `Portal(Backward, 0.8)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `NatGeoAnimator` to support NatGeo transition animation. It supports only a direction `NatGeo(direction)`, if no specified, the default values are `NatGeo(Left)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `Turn` to support Turn transition animation. It supports only a direction `Turn(direction)`, if no specified, the default values are `Turn(Left)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `CardsAnimator` to support Cards transition animation. It supports parameters `Cards(direction)`, if no specified, the default values are `Cards(Forward)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `FlipAnimator` to support Flip transition animation. It supports parameters `Flip(direction)`, if no specified, the default values are `Flip(Left)`. Currently only support `Flip(Left)` and `Flip(Right)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add `ContainerTransition` to manage transition animations between two UIViewController in a container
- Add `AnimatableCollectionViewCell` [#167](https://github.com/IBAnimatable/IBAnimatable/pull/167)
- Add `PinchInteractiveAnimator` to support `Pinch(Close)`, `Pinch(Open)` for `Pinch` gesture transition controller. [#125](https://github.com/IBAnimatable/IBAnimatable/issues/125)
- Add `SlideAnimator` to support Slide transition animation. It supports parameters `Slide(direction, fade)`, if no specified, the default values are `Flip(Left)`. [#155](https://github.com/IBAnimatable/IBAnimatable/issues/155)
- Add IBAnimatable Playground to demonstrate transitions and interactions. [#204](https://github.com/IBAnimatable/IBAnimatable/pull/204)
- Add `Parallelogram` mask. [#207 - Parallelogram Mask support in Maskdesignable](https://github.com/IBAnimatable/IBAnimatable/pull/207)
- Add `popToRootViewController` segue for poping to root ViewController of the NavigationController. [#212](https://github.com/IBAnimatable/IBAnimatable/pull/212)

#### Bugfixes

- Use `weak` for the `viewController` in `InteractiveAnimator` to avoid retain cycle.
- Fixed the right image of `SideImageDesignable` [#176](https://github.com/IBAnimatable/IBAnimatable/issues/176)
- Fix a bug to support single side of border for AnimatableTextField [#179](https://github.com/IBAnimatable/IBAnimatable/issues/179)
- `AnimatorFactory` and all the `***Animators` can now be used / instantiate outside of `IBAnimatable`

---
### [2.2](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.2)

#### API breaking changes

- Change `SystemPageCurlAnimator` to `SystemPageAnimator` to support `SystemPage(Curl)` and `SystemPage(UnCurl)` transition animations.

#### Enhancements

- `AnimatableLabel` now conforms `BorderDesignable`
- New transition animations [#126](https://github.com/IBAnimatable/IBAnimatable/issues/126):
    - `SystemSuckEffect`
    - `SystemRippleEffect`
    - `SystemMoveIn`
    - `SystemPush`
    - `SystemReveal`
    - `SystemRotate` to support:
         - `SystemRotate(90)`
         - `SystemRotate(90ccw)`
         - `SystemRotate(180)`
         - `SystemRotate(180ccw)`
         - => Note: It seems that only `SystemRotate(90)` is working as expected. `CATransition` issues?
    - `SystemCameraIrisAnimator` to support:
         - `SystemCameraIris`
         - `SystemCameraIris(HollowOpen)`
         - `SystemCameraIris(HollowClose)`
- Use framework in demo app [#149](https://github.com/IBAnimatable/IBAnimatable/pull/149)

#### Bugfixes

- Fix the sided borders issue [#150](https://github.com/IBAnimatable/IBAnimatable/pull/150)
- Fix the `FromTop` and `FromBottom` directions in system built-in animations [#156](https://github.com/IBAnimatable/IBAnimatable/pull/156)

---
### [2.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.1)

#### API breaking changes

- Remove `MaskDesignable` public methods ([#101](https://github.com/IBAnimatable/IBAnimatable/issues/101)):
   	- Remove `maskCircle()`, use `view.maskType = String(MaskType.Circle)` instead
   	- Remove `maskStar(_:)`, use `view.maskType = "Star(6)"` instead
   	- Remove `maskPolygon()`, use `view.maskType = String(MaskType.Polygon)` instead
   	- Remove `maskTriangle()`, use `view.maskType = String(MaskType.Triangle)` instead
   	- Remove `maskWave(_:_:_:)`, use `view.maskType = "Wave(up, 16, 40)"` instead
- Improve the options in `TransitionAnimationType` enum. ([#137](https://github.com/IBAnimatable/IBAnimatable/pull/137))
   	- Remove `SystemCubeFromLeft`, use `SystemCube(Left)`
   	- Remove `SystemCubeFromRight`, use `SystemCube(Right)`
   	- Remove `SystemCubeFromTop`, use `SystemCube(Top)`
   	- Remove `SystemCubeFromBottom`, use `SystemCube(Bottom)`
   	- Remove `SystemFlipFromLeft`, use `SystemFlip(Left)`
   	- Remove `SystemFlipFromRight`, use `SystemFlip(Right)`
   	- Remove `SystemFlipFromTop`, use `SystemFlip(Top)`
   	- Remove `SystemFlipFromBottom`, use `SystemFlip(Bottom)`

#### Enhancements

- Support Xcode 7.3 and Swift 2.2
- Configurable mask polygon (sides) [#112](https://github.com/IBAnimatable/IBAnimatable/issues/112)
- Add `SystemPageCurlAnimator` to support `SystemPageCurlFromTop` and `SystemPageCurlFromBottom` transition animations [#126](https://github.com/IBAnimatable/IBAnimatable/issues/126)
- `AnimatableLabel` now conforms `CornerDesignable` and `FillDesignable`
- Support Carthage 0.15.2 [#131](https://github.com/IBAnimatable/IBAnimatable/issues/131)

#### Bugfixes

- Fixed a bug that was making `GradientDesignable` not filling the dedicated frame [#129](https://github.com/IBAnimatable/IBAnimatable/issues/129)
- Fixed a bug that was making `MaskDesignable` not filling the dedicated frame

---
### [2.0](https://github.com/IBAnimatable/IBAnimatable/releases/tag/2.0)

#### API breaking changes

- Remove `DesignableViewController`, use `AnimatableViewController` instead.

#### Enhancements

- New IBAnimatable icon 🎊
- Add `AnimatableNavigationController` to support custom Push and Pop transition animations
- Add `AnimatableViewController` to support custom Present and Dismiss transition animations
- Add `SystemCubeAnimator` to support `SystemCubeFromLeft`, `SystemCubeFromRight`, `SystemCubeFromTop` and `SystemCubeFromBottom` transition animations
- Add `SystemFlipAnimator` to support `SystemFlipFromLeft`, `SystemFlipFromRight`, `SystemFlipFromTop` and `SystemFlipFromBottom` transition animations
- Add `FadeAnimator` to support `Fade`, `FadeIn` and `FadeOut` transition animations
- Add `CALayerExtension` to simplify CALayer animations with completion closure.
- Add `Navigator` to manage Push and Pop transition animations
- Add `Presenter` to manage Present and Dismiss transition animations
- Add `PresentFadeSegue`, `PresentFadeInSegue` and `PresentFadeOutSegue` for Present transition with Fade animations
- Add `PresentFadeWithDismissInteractionSegue`, `PresentFadeInWithDismissInteractionSegue` and `PresentFadeOutWithDismissInteractionSegue` for Present transition with Fade animations and getsture interactions.
- Add `PanInteractiveAnimator` to handle Pan interaction for Dismiss and Pop
- Demo App can experiment all transition animations (tap on "Forget Password" button to see)

#### Bugfixes

- Fix potential crash when using `GradientDesignable`
- Fix slideIn/Out animations on second screens (e.g. AirPlay)

---
### [1.2](https://github.com/IBAnimatable/IBAnimatable/releases/tag/1.2)

#### Enhancements

- Swift Package Manager support. [#5](https://github.com/IBAnimatable/IBAnimatable/issues/5)
- Predefined flat colors. [#71](https://github.com/IBAnimatable/IBAnimatable/issues/71)
- Customise mask draw from interface builder [#50](https://github.com/IBAnimatable/IBAnimatable/issues/50) [#8](https://github.com/IBAnimatable/IBAnimatable/issues/8) [#76](https://github.com/IBAnimatable/IBAnimatable/issues/76):
  - Star(6) -> draw star mask with 6 sides.
  - Wave(up,50,100) -> draw a wave up mask with 50 as width, and 100 as offset.
- Makes `BorderDesignable` usable in playground
- Add MoveTo and MoveBy animations [#74](https://github.com/IBAnimatable/IBAnimatable/issues/74)

#### Bugfixes

- Fixed `GradientDesignable` rotation. [#86](https://github.com/IBAnimatable/IBAnimatable/issues/86)
- Fixed `BorderDesignable` after rotation.
- Fixed mask star drawing bug. [#95](https://github.com/IBAnimatable/IBAnimatable/issues/95)
- Fixed the border color / width when used with a mask. [#95](https://github.com/IBAnimatable/IBAnimatable/issues/101)

### [1.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/1.1)

#### API breaking changes

- Remove `DesignableGradientView`, use `AnimatableView` to configure gradient. [#81](https://github.com/IBAnimatable/IBAnimatable/issues/81) and [#86](https://github.com/IBAnimatable/IBAnimatable/issues/86)

#### Enhancements

- New animations: Rotate, RotateCCW [#51](https://github.com/IBAnimatable/IBAnimatable/issues/51)
- New masks: Star, Triangle, Polygon, Wave
- SidebarImage now support right images
- Predefined gradients [#24](https://github.com/IBAnimatable/IBAnimatable/issues/24)
- iOS8 support [#89](https://github.com/IBAnimatable/IBAnimatable/issues/89)

#### Bugfixes

- Fixed left gradient
- Fixed slideOut / slideIn animations [#46](https://github.com/IBAnimatable/IBAnimatable/issues/46)

---
### [1.0.1](https://github.com/IBAnimatable/IBAnimatable/releases/tag/1.0.1)

#### Enhancements

- Carthage support - [#6](https://github.com/IBAnimatable/IBAnimatable/issues/6)

---
### [1.0](https://github.com/IBAnimatable/IBAnimatable/releases/tag/1.0)

- Initial release


