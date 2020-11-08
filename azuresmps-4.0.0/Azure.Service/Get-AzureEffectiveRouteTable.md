---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106353"
---
# Get-AzureEffectiveRouteTable

## SYNOPSIS
Bir sanal makinede uygulanan rotayı alır.

## INDEKI

### IaaSGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SlotGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureEffectiveRouteTable** cmdlet 'i, bir sanal makinede uygulanan rotayı alır.
Bu işlemin tamamlanması birkaç saniye sürebilir.

## ÖRNEKLERDEN

### Örnek 1: sanal makineyi uygulama
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

Bu komut, ContosoService adındaki hizmet için ContosoVM06 adındaki bir sanal makineyi alır ve bu sanal makine nesnesini geçerli cmdlet 'e geçirir.
Geçerli cmdlet, bu sanal makineye uygulanan rotayı alır.

## PARAMETRELERINE

### -Networkınterfacename
Bu cmdlet 'in etkin yollar aldığı ağ bağdaştırıcısının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstanceName
Bu cmdlet 'in etkin yolları aldığı PaaS rolünün adını belirtir.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Bulut hizmetinin adını belirtir.
Bu cmdlet 'in geçerli yollarla kullandığı PaaS rolü, bu parametrenin belirttiği hizmete aittir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
PaaS yuvasını belirtir.
Bu cmdlet 'in geçerli yolların aldığı PaaS rolünde bu parametrenin belirttiği yuva vardır.
Geçerli değerler: 

- Üretim
- Geçici saklama 

Varsayılan değer Production değeridir.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Bu cmdlet 'in geçerli yolları aldığı sanal makine nesnesini belirtir.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### System. topluluklar. Generic. IEnumerable<Microsoft. Windowsazme. Management. Network. modeller. EffectiveRouteTable, Microsoft. Windowsazme. Management. Network>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRouteTable](./Get-AzureRouteTable.md)

[Yeni-AzureRouteTable](./New-AzureRouteTable.md)

[Remove-AzureRouteTable](./Remove-AzureRouteTable.md)

[Remove-Azuyeniden yönlendirme](./Remove-AzureSubnetRouteTable.md)

[Set-Azuyeniden gönderiliyor Netroutetable](./Set-AzureSubnetRouteTable.md)


