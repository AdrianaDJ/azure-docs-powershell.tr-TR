---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277192"
---
# Unregister-AzStackHCI

## SYNOPSIS
Unregister-AzStackHCI, şirket içi kümeyi temsil eden Microsoft. AzureStackHCI bulut kaynağını silip şirket içi kümenin Azure ile kaydını siler.
Hiçbir parametre geçirilmemişse kümenin kaydını kaldırmak için, kümedeki kullanılabilir olan kayıt bilgileri kullanılır.

## INDEKI

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Unregister-AzStackHCI, şirket içi kümeyi temsil eden Microsoft. AzureStackHCI bulut kaynağını silip şirket içi kümenin Azure ile kaydını siler.
Hiçbir parametre geçirilmemişse kümenin kaydını kaldırmak için, kümedeki kullanılabilir olan kayıt bilgileri kullanılır.

## ÖRNEKLERDEN

### ÖRNEK 1
```
Invoking on one of the cluster node
```

C:\PS \> Unregister-AzStackHCI sonucu: başarı

### ÖRNEK 2
```
Invoking from the management node
```

C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 sonucu: başarı

### ÖRNEK 3
```
Invoking from WAC
```

C:\PS \> Unregister-Azstackhcı-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken.. rerrer-AccountID user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-confirm: $false sonucu: başarı

### ÖRNEK 4
```
Invoking with all the parameters
```

C:\PS \> kaydını-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-resourceName HciCluster1-tenan"c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ... rerrer-AccountID user1@corp1.com -environmentname Azurecsesli-ComputerName node1hci-Credential Get-Credential Result: Success

## PARAMETRELERINE

### -SubscriptionID
Kaynağı oluşturmak için Azure aboneliğini belirtir

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

### -ResourceName
Azure 'da oluşturulan kaynağın kaynak adını belirtir.
Belirtilmemişse, şirket içi küme adı kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenantıd
Azure Tenantıd 'yi belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure Resource grubunun adını belirtir.
Belirtilmemişse \<LocalClusterName\> -RG kaynak grubu adı olarak kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
ARM erişim belirtecini belirtir.
GraphAccessToken ve AccountID ile birlikte bunu belirtmek için Azure etkileşimli oturum açma önlenir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Grafik erişim belirtecini belirtir.
ArmAccessToken ve AccountID ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
ARM erişim belirtecini belirtir.
ArmAccessToken ve GraphAccessToken ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Azure ortamını belirtir.
Varsayılan olarak Azurecyüksek.
Geçerli değerler Azurecyüksek, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Azure 'a kaydolan şirket içi kümesindeki küme düğümünden birini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
ComputerName kimlik bilgisini belirtir.
Varsayılan, cmdlet 'ı yürüten geçerli kullanıcıdır.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

## ÇıKıŞLAR

### PSCustomObject. PSCustomObject 'de aşağıdaki özellikleri döndürür
### Sonuç: başarılı veya başarısız oldu ya da Iptal edildi.
## NOTLARıNDA

## ILGILI BAĞLANTıLAR
