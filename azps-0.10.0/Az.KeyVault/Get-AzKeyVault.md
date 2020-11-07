---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935804"
---
# Get-AzKeyVault

## SYNOPSIS
Tuş

## INDEKI

### GetVaultByName
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Bydeletedkasası
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Listalldeletedvaultsınsubscription
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listallvaultsınsubscription
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azanahtarkasası** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır. Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.

Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.

## ÖRNEKLERDEN

### Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın
```
PS C:\>Get-AzKeyVault
```

Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.

### Örnek 2: belirli bir Anahtar Kasası alma
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

Bu komut geçerli aboneliğinizde Contoso03Vault adındaki Anahtar Kasası 'nı alır ve $MyVault değişkeninde depolar. Anahtar Kasası hakkındaki ayrıntıları almak için $MyVault özelliklerini inceleyebilirsiniz.

### Örnek 3: kaynak grubundaki tuş örneklerini alma
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.

### Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma
```
PS C:\>Get-AzKeyVault -InRemovedState
```

Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.

### Örnek 5: silinen bir Anahtar Kasası alma
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Bu komut, geçerli aboneliğinizde ve eastus2 bölgesinde Contoso03Vault adlı silinmiş Anahtar Kasası bilgilerini alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inremovevseçstate
Çıktıda önceden silinmiş olan kasa gösterilip gösterilmeyeceğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Silinmiş kasanın konumu.

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sorgulanan Anahtar Kasası veya anahtar kasası ile ilişkili kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin:

@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Anahtar Kasası adını belirtir.

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. Pskasa

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Psvaultidentityıtem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDon kasa

### System. topluluklar. Generic. LIST ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkasa]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Aztuş Kasası](./New-AzKeyVault.md)

[Remove-Aztuş Kasası](./Remove-AzKeyVault.md)
