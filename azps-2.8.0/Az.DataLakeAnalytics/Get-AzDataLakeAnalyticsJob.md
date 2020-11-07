---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 73a9325ea4f1bc45eaaf2fb81796d526c7b95fea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752399"
---
# Get-AzDataLakeAnalyticsJob

## SYNOPSIS
Data Lake Analytics işini alır.

## INDEKI

### GetAllInResourceGroupAndAccount (varsayılan)
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getbyspecificjobınformation
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azdatalakeanaliz Ticsjob** cmdlet 'ı bir Azure Data Lake Analytics işini alır.
İş belirtmezseniz, bu cmdlet tüm işleri alır.

## ÖRNEKLERDEN

### Örnek 1: belirtilen işi edinme
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

Bu komut belirtilen KIMLIĞE sahip işi alır.

### Örnek 2: geçen hafta gönderilen işleri alma
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

Bu komut, geçen hafta gönderilen işleri alır.

## PARAMETRELERINE

### -Hesap
Veri Lake Analytics hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Include
İş hakkında alınacak ek bilgi türünü belirten seçenekleri belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Yabilirsiniz
- DebugInfo
- İstatistik
- Tüm

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Alınacak işin KIMLIĞINI belirtir.

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Ad
İş listesi sonuçlarını filtrelemek için kullanılacak bir ad belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Yabilirsiniz
- DebugInfo
- İstatistik
- Tüm

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pipelineıd
Belirtilen ardışık düzenin yalnızca işlerin bir bölümünü gösteren isteğe bağlı KIMLIK.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
Yalnızca belirtilen yinelenme işlerinin bir bölümünü gösteren isteğe bağlı bir KIMLIK.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sonuç
İş sonuçları için bir sonuç filtresi belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Yabilirsiniz
- İptal
- Erişilemedi
- Oluşturuldu

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Durumlu
İş sonuçları için bir durum filtresi belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Benimsen
- Yeni
- Derleyip
- Planlamayı
- Sıradan
- Başlarken
- Dığında
- Çalışması
- Sonlandırdı

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedAfter
Bir tarih filtresi belirtir.
İş listesi sonucuna belirtilen tarihten sonra gönderilen işlere filtre uygulamak için bu parametreyi kullanın.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Submittedbir
Bir tarih filtresi belirtir.
İş listesi sonucuna belirtilen tarihten önce gönderilen işlere filtre uygulamak için bu parametreyi kullanın.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Gönderenin
Bir kullanıcının e-posta adresini belirtir.
İş listesi sonuçlarını belirli bir kullanıcı tarafından gönderilen işlere filtre uygulamak için bu parametreyi kullanın.

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Üst
Döndürülecek iş sayısını belirten isteğe bağlı bir değer. Varsayılan değer 500

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Guid

### Microsoft. Azure. Commands. DataLakeAnalytics. model. Datalakeanalizleri Ticsenums + ExtendedJobData

### System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### Microsoft. Azure. Management. DataLake. Analytics. modeller. JobState []

### Microsoft. Azure. Management. DataLake. Analytics. modeller. JobResult []

### System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

## ÇıKıŞLAR

### Microsoft. Azure. Management. DataLake. Analytics. modeller. Jobınformation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Stop-Azdatalakeanaliz Ticsjob](./Stop-AzDataLakeAnalyticsJob.md)

[Submit-Azdatalakeanaliz Ticsjob](./Submit-AzDataLakeAnalyticsJob.md)

[Wait-Azdatalakeanalyzer](./Wait-AzDataLakeAnalyticsJob.md)


