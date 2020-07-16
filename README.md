# UniCustomLateUpdateManager

## 使用例

```cs
using Kogane;
using UnityEngine;

public class Example : MonoBehaviour, ILateUpdatable
{
    private void OnEnable()
    {
        CustomLateUpdateManager.Add( this );
    }

    private void OnDisable()
    {
        CustomLateUpdateManager.Remove( this );
    }

    void ILateUpdatable.OnLateUpdate()
    {
        Debug.Log( "ピカチュウ" );
    }
}
```