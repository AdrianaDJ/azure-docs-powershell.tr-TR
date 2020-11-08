---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108603"
---
# Get-AzStorageFile

## SYNOPSIS
Bir yolun dizinlerini ve dosyalarını listeler.

## INDEKI

### PaylaşımAdı (varsayılan)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Paylaş
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Directory
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Tanım
**Get-AzStorageFile** cmdlet 'i belirttiğiniz paylaşımın veya dizinin dizinlerini ve dosyalarını listeler.
Belirtilen yoldaki bir dizinin veya dosyanın bir örneğinin alınacağı *yol* parametresini belirtin.
Bu cmdlet, **Azurestoragefile** ve **Azurestoragedirectory** nesnelerini döndürür.
Dosya ve klasörleri birbirinden ayırt etmek için **IsDirectory** özelliğini kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: paylaşımdaki dizinleri listeleme
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

Bu komut yalnızca paylaşım ContosoShare06 dizinleri listeler.
Önce hem dosyaları hem de dizinleri alır, ardışık düzen işlecini kullanarak bunları **WHERE** operatörüne geçirir ve sonra türü "AzureStorageFileDirectory" olan tüm nesneleri atar.

### Örnek 2: dosya dizini listeleme
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Bu komut, Share ContosoShare06 'in altındaki Contosoworkingklasöründeki dosya ve klasörleri listeler.
Önce dizin örneğini alır ve ardından dizini listelemek için **Get-AzStorageFile** cmdlet 'ine ardışık düzen.

## PARAMETRELERINE

### -ClientTimeoutPerRequest
Bir hizmet isteği için istemci tarafı zaman aşımı aralığını saniye cinsinden belirtir.
Önceki çağrı belirtilen aralıkta başarısız olursa, bu cmdlet isteği yeniden dener.
Bu cmdlet Aralık geçmeden önce başarılı bir yanıt almadıysa, bu cmdlet hata döndürür.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Maksimum eşzamanlı ağ çağrılarını belirtir.
Eş zamanlı ağ çağrılarının maksimum sayısını belirterek, eşzamanlılığı yerel CPU ve bant genişliği kullanımını kısıtlayacak şekilde sınırlandırmak için bu parametreyi kullanabilirsiniz.
Belirtilen değer mutlak bir sayı ve çekirdek sayısıyla çarpılmadı.
Bu parametre, düşük bant genişliği ortamlarındaki ağ bağlantısı sorunlarının azaltılmasına yardımcı olabilir; Örneğin, 100 kilobit/saniye.
Varsayılan değer 10 ' dır.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure depolama bağlamını belirtir.
Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dizin
Bir klasörü **Cloudfiledirectory** nesnesi olarak belirtir.
Bu cmdlet, bu parametrenin belirttiği klasörü alır.
Dizin edinmek için New-AzStorageDirectory cmdlet 'ini kullanın.
Ayrıca **Get-AzStorageFile** cmdlet 'ini kullanarak bir dizin elde edebilirsiniz.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Yol
Klasörün yolunu belirtir.
*Yol* parametresini atlarsanız, **Get-azstoragefile** belirtilen dosya paylaşımında veya dizininde bulunan dizinleri ve dosyaları listeler.
*Yol* parametresini eklerseniz, **Get-azstoragefile** belirtilen yoldaki dizinin veya dosyanın bir örneğini döndürür.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
İstek için, saniye cinsinden hizmet tarafı zaman aşımı aralığını belirtir.
Belirtilen Aralık hizmet isteği işlemeden önce sona erdiğinde, depolama hizmeti hata döndürür.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paylaşım
Bir **Cloudfileshare** nesnesi belirtir.
Bu cmdlet, bu parametrenin belirttiği dosya paylaşımından bir dosya veya dizin alır.
**Cloudfileshare** nesnesi edinmek için Get-AzStorageShare cmdlet 'ini kullanın.
Bu nesne depolama bağlamını içerir.
Bu parametreyi belirtirseniz, *bağlam* parametresini belirtmeyin.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PaylaşımAdı
Dosya paylaşımının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği dosya paylaşımından bir dosya veya dizin alır.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Storage. File. CloudFileShare

### Microsoft. Azure. Storage. File. CloudFileDirectory

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageFile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[Yeni-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


