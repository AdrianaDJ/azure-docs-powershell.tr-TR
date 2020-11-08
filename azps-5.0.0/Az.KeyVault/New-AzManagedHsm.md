---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280210"
---
# New-AzManagedHsm

## SYNOPSIS
Yönetilen bir HSM oluşturur.

## INDEKI

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzManagedHsm** cmdlet 'i belirtilen kaynak grubunda YÖNETILEN bir HSM oluşturur. Yönetilen HSM 'de anahtar eklemek, kaldırmak veya listelemek için, kullanıcının yönetici 'ye Kullanıcı KIMLIĞI ekleyerek izinleri vermesi gerekir.

## ÖRNEKLERDEN

### Örnek 1: StandardB1 yönetimli bir HSM oluşturma
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Bu komut, eastus2euap konumunda myhsm adlı bir yönetilen HSM oluşturur. Komut, yönetilen HSM 'yi myrg1 adlı kaynak grubuna ekler. Komut, *SKU* parametresi için bir değer belirtmediğinden, Standard_B1 YÖNETIMLI bir HSM oluşturur.

### Örnek 2: CustomB32 yönetimli bir HSM oluşturma
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

Bu komut, önceki örnekte olduğu gibi, yönetilen bir HSM oluşturur. Bununla birlikte, CustomB32 yönetimli bir HSM oluşturmak için *SKU* parametre CustomB32 değerini belirtir.

## PARAMETRELERINE

### -Yönetici
Bu yönetilen HSM havuzu için ilk yönetici nesne kimliği.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Anahtar Kasası oluşturacağınız Azure bölgesini belirtir.
Seçimlerinizi görmek için komut Get-AzResourceProvider ProviderNamespace parametresiyle birlikte kullanın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Oluşturulacak yönetilen HSM 'in adını belirtir.
Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.
Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.
Ad, evrensel olarak benzersiz olmalıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Yönetilen HSM örneğinin SKU adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketlerini temsil eden karma bir tablo.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. String []

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzManagedHsm](./Get-AzManagedHsm.md)

[Remove-AzManagedHsm](./Remove-AzManagedHsm.md)

[Güncelleştirme-AzManagedHsm](./Update-AzManagedHsm.md)