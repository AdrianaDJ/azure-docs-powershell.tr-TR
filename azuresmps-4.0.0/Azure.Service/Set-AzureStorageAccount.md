---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105850"
---
# Set-AzureStorageAccount

## SYNOPSIS
Bir Azure aboneliğindeki depolama hesabının özelliklerini güncelleştirir.

## INDEKI

### AccountType (varsayılan)
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GeoReplicationEnabled
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Set-AzureStorageAccount** cmdlet 'i, geçerli abonelikteki bir Azure depolama hesabının özelliklerini güncelleştirir.
Ayarlanabilir özellikler şunlardır: **etiket** , **Açıklama** , **tür** ve **GeoReplicationEnabled**.

## ÖRNEKLERDEN

### Örnek 1: depolama hesabının etiketini güncelleştirme
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

Bu komut, ContosoStorage01 adlı depolama hesabının **etiket** ve **Açıklama** özelliklerini güncelleştirir.

### Örnek 2: depolama hesabı için coğrafi çoğaltma özelliğini etkinleştirme
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

Bu komut, ContosoStorage01 adlı depolama hesabı için **GeoReplicationEnabled** özelliğini $false olarak ayarlar.

### Örnek 3: depolama hesabı için Coğrafi çoğaltmayı devre dışı bırakma
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

Bu komut, ContosoStorage01 adlı depolama hesabı için **GeoReplicationEnabled** özelliğini $true olarak ayarlar.

## PARAMETRELERINE

### -Açıklama
Depolama hesabı için bir açıklama belirtir.
Açıklama 1024 karakter uzunluğunda olabilir.

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

### -GeoReplicationEnabled
Depolama hesabının coğrafi çoğaltma 'nın etkin olup olmadığını belirtir.

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
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

### Etiketli
Depolama hesabı için bir etiket belirtir.
Etiket en çok 100 karakter uzunluğunda olabilir.

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

### -StorageAccountName
Bu cmdlet 'in değiştirdiği depolama hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Depolama hesabının türünü belirtir.
Geçerli değerler: 

- Standard_LRS
- Standard_ZRS
- Standard_GRS
- Standard_RAGRS
- Premium_LRS

Bu parametre belirtilmezse, varsayılan değer Standard_GRS olur.

*GeoReplicationEnabled* parametresini belirtmenin etkisi, *tür* parametresinde Standard_GRS belirtmeyle aynıdır.

Standard_ZRS veya Premium_LRS hesapları diğer hesap türleriyle değiştirilemez.

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
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

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Yeni-AzureStorageAccount](./New-AzureStorageAccount.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)


