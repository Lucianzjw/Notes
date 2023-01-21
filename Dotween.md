#Dotween常用方法或组合



##特定组件的方法

1. Aduio Mixer:

   ```c#
   DOSetFloat(string floatName, float to, float duration);
   ```

2. Audio Soucer

   ```c#
   DOFade(float to, float duration)
   DOPitch(float to, float duration)
   ```

3. Camera

   ```c#
   DOAspect(float to, float duration)
   DOColor(Color to, float duration)
   DOFarClipPlane(float to, float duration)
   DOFieldOfView(float to, float duration)
   DONearClipPlane(float to, float duration)
   DOOrthoSize(float to, float duration)
   DOPixelRect(Rect to, float duration)
   DORect(Rect to, float duration)
   DOShakePosition(float duration, float/Vector3 strength, int vibrato, bool fadeOut)
   DOShakeRotation(float duration, float/Vector3 strength, int vibrato, float randomness bool fadeOut)
   ```

4. Light

   ```c#
   DOColor(Color to, float duration)
   DOIntensity(float to, float duration)
   DOShadowStrength(float to, float duration)
   //可混合的补间
   DOBlendableColor(Color to, float duration)
   ```

5. LineRenderer

   ```c#
   DOColor(Color2 startValue, Color2 endValue, float duration)
   ```

6. Material

   ```c#
   DOColor(Color to, float duration)
   DOColor(Color to, string property, float duration)
   DOFade(float to, float duration)
   DOFade(float to, string property, float duration)
   DOFloat(float to, string property, float duration)
   DOGradientColor(Gradient to, float duration)
   DOGradientColor(Gradient to, string property, float duration)
   DOOffset(Vector2 to, float duration)
   DOOffset(Vector2 to, string property, float duration)
   DOTiling(Vector2 to, float duration)
   DOTiling(Vector2 to, string property, float duration)
   DOVector(Vector4 to, string property, float duration)
   //可混合的补间
   DOBlendableColor(Color to, float duration)
   DOBlendableColor(Color to, string property, float duration)
   ```

7. Rigidbody

   ```c#
   DOMove（Vector3 to，float duration，bool snapping）
   DOMoveX / DOMoveY / DOMoveZ（float to，float duration，bool snapping）
   DOJump（Vector3 endValue，float jumpPower，int numJumps，float duration，bool snapping）
   ```

8. Rotate

   ```c#
   DORotate(Vector3 to, float duration, RotateMode mode)
   DOLookAt(Vector3 towards, float duration, AxisConstraint axisConstraint = AxisConstraint.None, Vector3 up = Vector3.up)
   PRO ONLY ➨ Spiral – no FROM
   DOSpiral(float duration, Vector3 axis = null, SpiralMode mode = SpiralMode.Expand, float speed = 1, float frequency = 10, float depth = 0, bool snapping = false)
   ```

9. SpriteRenderer

   ```c#
   DOColor(Color to, float duration)
   DOFade(float to, float duration)
   DOGradientColor(Gradient to, float duration)
    //可混合的补间
   DOBlendableColor(Color to, float duration)
   ```

10. TrailRenderer

    ```c#
    DOResize(float toStartWidth, float toEndWidth, float duration)
    DOTime(float to, float duration)
    ```

11.  

##数字的补间

Dotween.To:

从一个数字在一定时间time内转变为另外一个数字

其中

Getter:	() => startVolume

Setter:	x => startVolume = x

```c#
//公式
DOTween.To(() => startVolume, x => startVolume = x, endvolume, time);

//Example
Dotween.To(()=> a,x=>a=x,10,5);

```