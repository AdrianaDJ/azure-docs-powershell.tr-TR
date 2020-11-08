---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106432"
---
# Set-AzureAclConfig

## SYNOPSIS
ACL yapılandırma nesnesini değiştirir.

## INDEKI

### AddRule
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### RemoveRule
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### SetRule
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Set-AzureAclConfig** cmdlet 'i, var olan Azure sanal makine yapılandırmasından bir erişim denetim LISTESI (ACL) yapılandırma nesnesini değiştirir.

## ÖRNEKLERDEN

### Örnek 1: yeni bir ACL yapılandırmasına kural ekleme
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

İlk komut bir ACL yapılandırması oluşturur ve $Acl değişkeninde depolar.

İkinci komut, $Acl depolanan yapılandırmaya yeni bir kural ekler.
Komut, kuralın bir eylemini, alt ağını, sıralamasını ve açıklamasını belirtir.

### Örnek 2: ACL yapılandırmasındaki bir kuralı değiştirme
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

İlk komut, VirtualMachine07 adındaki sanal makineyi, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette alır.
Komut, bu nesneyi ardışık düzen işlecini kullanarak **Get-AzureAclConfig** cmdlet 'ine geçirir.
Bu cmdlet Web adlı uç noktanın ACL yapılandırmasını alır.
Komut bu ACL yapılandırma nesnesini $Acl değişkeninde depolar.

İkinci komut, KIMLIĞI 0 olan kuralı değiştirir.
Komut, kuralın sırasını ve açıklamasını değiştirir.

Son komutu, **set-AzureEndpoint** cmdlet 'ini kullanarak bu sanal makinenin ACL yapılandırma nesnesini ayarlar.
Bu komut, bu sanal makineyi de güncelleştirir.

### Örnek 3: ACL yapılandırmasından kural kaldırma
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

İlk komut $Acl değişkeninde bir ACL yapılandırma nesnesini depolar.
Bu, önceki örnekle aynıdır.

İkinci komut, KIMLIĞI 0 olan kuralı $Acl ACL yapılandırmasından kaldırır.

Son komutu sanal makinenin ACL yapılandırma nesnesini ayarlar ve bu sanal makineyi güncelleştirir.
Bu, önceki örnekle aynıdır.

## PARAMETRELERINE

### -ACL
Bu cmdlet 'in değiştirdiği bir ACL yapılandırma nesnesi belirtir.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Eylem
Bu cmdlet 'in eklediği veya değiştirdiği kuralın eylemini belirtir.
Geçerli değerler: Izin ver ve Reddet.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRule
Bu cmdlet 'in ACL yapılandırmasına kural eklediğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Açıklama
Bu cmdlet 'in eklediği veya değiştirdiği kuralın açıklamasını belirtir.

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Düzen
Bu cmdlet 'in eklediği veya değiştirdiği kuralın işlem sırasını belirtir.

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteSubnet
Bu cmdlet 'in eklediği veya değiştirdiği kuralın uzaktaki alt ağını belirtir.
Sınıfsız Etki alanları arası yönlendirme (CıDR) biçimindeki bir adresi belirtir.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRule
Bu cmdlet 'in ACL yapılandırmasından kural kaldırmadığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleId
Bu cmdlet 'in kaldırdığı veya ACL yapılandırması için değiştirdiği kuralın KIMLIĞINI belirtir.

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetRule
Bu cmdlet 'in ACL yapılandırmasındaki bir kuralı değiştirdiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureAclConfig](./New-AzureAclConfig.md)

[Remove-AzureAclConfig](./Remove-AzureAclConfig.md)

[Set-AzureEndpoint](./Set-AzureEndpoint.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


