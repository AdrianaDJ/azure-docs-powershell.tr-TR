---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106057"
---
# Set-AzureEndpoint

## SYNOPSIS
Bir sanal makineye atanan uç noktayı değiştirir.

## INDEKI

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Set-AzureEndpoint** cmdlet 'ı bir Azure sanal makinesine atanmış uç noktayı değiştirir.
Yük dengeli olmayan bir son noktadaki değişikliklerini belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: bir bağlantı noktasını dinlemek için uç noktayı değiştirme
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak VirtualMachine01 adındaki sanal makinenin yapılandırmasını alır.
Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.
Bu cmdlet, bağlantı noktası 443 ' i dinlemek için Web adındaki uç noktayı değiştirir.
Komut, sanal makine nesnesini, değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.

## PARAMETRELERINE

### -ACL
Bu cmdlet 'in uç noktaya uyguladığı bir erişim denetim listesi (ACL) yapılandırma nesnesini belirtir.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectServerReturn
Bu cmdlet 'in doğrudan sunucu döndürülmesini etkinleştirilip etkinleştirilmediğini belirtir.
Etkinleştirmek için $True veya devre dışı bırakmak için $False belirtin.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Idfaizzamansayısı
Uç noktanın TCP boşta kalma zaman aşımı süresini dakika olarak belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -Internalloadbalancername
İç yük dengeleyicinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerDistribution
Yük dengeleyici dağıtım algoritmasını belirtir.
Geçerli değerler: 

- sourceIP.
İki demet benzeşim: kaynak IP, hedef IP 
- Sourceıpprotocol.
Üç demet benzeşim: kaynak IP, hedef IP, protokol 
- yabilirsiniz.
Beş demet benzeşim: kaynak IP, kaynak bağlantı noktası, hedef IP, hedef bağlantı noktası Protokolü 

Varsayılan değer yok 'tur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPort
Bu uç noktanın kullandığı yerel, özel bağlantı noktasını belirtir.
Sanal makinedeki uygulamalar bu bağlantı noktasında bu uç nokta için hizmet giriş isteklerini dinler.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Uç noktasının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -İletişim kuralı
Uç noktasının protokolünü belirtir.
Geçerli değerler: 

- TC 
- UDP

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicPort
Uç noktanın kullandığı ortak bağlantı noktasını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualIPName
Azure 'un uç noktayla ilişki kurduğu sanal IP adresinin adını belirtir.
Hizmetiniz birden çok sanal IP 'ye sahip olabilir.
Sanal IP 'Ler oluşturmak için **Add-AzureVirtualIP** cmdlet 'ini kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Uç noktanın ait olduğu sanal makineyi belirtir.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

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

### System. Object

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureEndpoint](./Add-AzureEndpoint.md)

[Add-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureEndpoint](./Remove-AzureEndpoint.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


