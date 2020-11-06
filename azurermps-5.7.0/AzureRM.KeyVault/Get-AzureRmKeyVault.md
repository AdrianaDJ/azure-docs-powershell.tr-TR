---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594953"
---
# Get-AzureRmKeyVault

## SYNOPSIS
Tuş

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Listallvaultsınsubscription (varsayılan)
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetVaultByName
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Bydeletedkasası
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listalldeletedvaultsınsubscription
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermkeykasa** cmdlet 'i, bir abonelikteki Anahtar Kasası hakkında bilgi alır. Bir abonelikteki tüm önemli kasa örneklerini görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir anahtar kasaya göre filtreleyebilirsiniz.

Tek bir Anahtar Kasası aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.

## ÖRNEKLERDEN

### Örnek 1: geçerli aboneliğinizdeki tüm tuş örneklerini alın
```
PS C:\>Get-AzureRMKeyVault
```

Bu komut geçerli aboneliğinizdeki tüm anahtarı getirir.

### Örnek 2: belirli bir Anahtar Kasası alma
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

Bu komut geçerli aboneliğinizde Contoso03Vault adındaki Anahtar Kasası 'nı alır ve $MyVault değişkeninde depolar. Anahtar Kasası hakkındaki ayrıntıları almak için $MyVault özelliklerini inceleyebilirsiniz.

### Örnek 3: kaynak grubundaki tuş örneklerini alma
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Bu komut, ContosoPayRollResourceGroup adlı kaynak grubundaki tüm anahtarı getirir.

### Örnek 4: geçerli aboneliğinizde tüm silinmiş anahtar örneklerini alma
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

Bu komut geçerli aboneliğinizde tüm silinmiş anahtar yerlerini alır.

### Örnek 5: silinen bir Anahtar Kasası alma
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Bu komut, geçerli aboneliğinizde ve eastus2 bölgesinde Contoso03Vault adlı silinmiş Anahtar Kasası bilgilerini alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Position: 1
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
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDEleditedtuş Kasası

### System. topluluklar. Generic. LIST ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeykasa]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermkeykasası](./New-AzureRmKeyVault.md)

[Remove-Azurermkeykasası](./Remove-AzureRmKeyVault.md)
