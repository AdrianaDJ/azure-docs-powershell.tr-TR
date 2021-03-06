---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 5fb8c8f71366dd9fd0a2c6b12fc023c1ce3ccf9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593479"
---
# Update-AzureRmMlWebService

## SYNOPSIS
Var olan bir Web hizmeti kaynağının özelliklerini güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### UpdateFromParameters
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateFromObject
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Update-AzureRmMlWebService cmdlet 'i, Web servisinin statik olmayan özelliklerini güncelleştirmenize olanak tanır.
Cmdlet, düzeltme eki olarak çalışır.
Yalnızca değişiklik yapmak istediğiniz özellikleri geçirin.

## ÖRNEKLERDEN

### --------------------------Örnek 1: seçmeli güncelleştirme bağımsız değişkenleri--------------------------
```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

Burada, Web hizmeti için çalışma zamanı sırasında açıklama, birincil erişim anahtarı değiştirilir ve tüm izlemeler için tanılama koleksiyonunu etkinleştirmelisiniz.

### --------------------------Örnek 2: bir Web hizmeti örneğine dayalı güncelleştirme--------------------------
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

Örnek ilk olarak yalnızca güncelleştirilecek alanları içeren bir Web hizmeti tanımı oluşturur ve ardından, bu dosyaları ServiceUpdates parametresini kullanarak uygulamak için Update-AzureRmMlWebService çağırır.

## PARAMETRELERINE

### -Kıymetler
Web hizmetini oluşturan varlık kümesi (örneğin modüller, veri kümeleri).

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Açıklama
Web hizmeti açıklamasına yönelik yeni değer.
Bu, hizmetin Swagger API şemasında görülebilir.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tanılama
Web hizmeti için tanılama izlemeleri koleksiyonunu denetleyen ayarlar.

```yaml
Type: DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Onay sorma.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Giriş
Swagger şema yapısı olarak sağlanan Web hizmeti girdisinin tanımı.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsReadOnly
Bu Web hizmetisalt okunur olarak belirtir.
Bir kez ayarlandıktan sonra, bu özelliğin değerini değiştirmek de içinde olmak üzere Web hizmeti artık güncelleştirilebilir ve yalnızca silinebilir.

```yaml
Type: SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Tuşları
Hizmetin çalışma zamanı API 'Lerine çağrı kimliklerinin doğrulanması için kullanılan erişim anahtarlarının birini veya her ikisini birden güncelleştirir.

```yaml
Type: WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Güncelleştirilecek Web hizmeti kaynağının adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Çıktı
Swagger şema yapısı olarak sağlanan Web hizmeti çıkışının (s) tanımı.

```yaml
Type: ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package
Bu Web hizmetini tanımlayan grafik paketinin tanımı.

```yaml
Type: GraphPackage
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parametreler
Web hizmeti için tanımlanmış, genel parametre adı olarak belirtilen genel parametre değerleri kümesi- \> varsayılan değer koleksiyonu.
Varsayılan bir değer belirtilmemişse, parametre gerekli kabul edilir.

```yaml
Type: Hashtable
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RealtimeConfiguration
Hizmetin gerçek uç noktası yapılandırmasına yönelik güncelleştirmeler.

```yaml
Type: RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Güncelleştirilecek Web servisini içeren kaynak grubu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceUpdates
Web hizmeti tanımı örneği olarak sağlanan Web hizmetine uygulanacak güncelleştirmeler kümesi.
Yalnızca statik olmayan alanlar değiştirilir.

```yaml
Type: WebService
Parameter Sets: UpdateFromObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountKey
Web hizmetiyle ilişkili depolama hesabının erişim tuşunu döndürür.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlık
Web hizmeti unvanı için yeni değer.
Bu, hizmetin Swagger API şemasında görülebilir.

```yaml
Type: String
Parameter Sets: UpdateFromParameters
Aliases: 

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Konumundaki
' ServiceUpdates ' parametresi ardışık düzenin ' WebService ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web
Azure Machine Learning Web hizmetinin Özet açıklaması.
Var olan bir Web hizmetinde Get-AzureRmMlWebService cmdlet 'i çağırarak döndürülen açıklamaya benzer.
Bu açıklama, depolama hesabının kimlik bilgileri ve hizmetin erişim tuşları gibi hassas özellikler içermez.

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml

## ILGILI BAĞLANTıLAR

