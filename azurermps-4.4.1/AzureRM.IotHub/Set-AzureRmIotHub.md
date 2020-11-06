---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: aad54e42d628239f087e376eabe6b9950c07b6f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594263"
---
# <span data-ttu-id="af576-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="af576-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="af576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af576-102">SYNOPSIS</span></span>
<span data-ttu-id="af576-103">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af576-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af576-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af576-104">SYNTAX</span></span>

### <span data-ttu-id="af576-105">UpdateSku (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af576-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="af576-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="af576-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="af576-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-109">Updateoperationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="af576-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="af576-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="af576-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af576-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="af576-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af576-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="af576-113">DESCRIPTION</span></span>
<span data-ttu-id="af576-114">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af576-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="af576-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af576-115">EXAMPLES</span></span>

### <span data-ttu-id="af576-116">Örnek 1 STB 'yi güncelleyin</span><span class="sxs-lookup"><span data-stu-id="af576-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="af576-117">"Myiothub" adlı IotHub için STB 'yi S1 ve birimler 'i 5 olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="af576-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="af576-118">Örnek 2 eventhub özelliklerini güncelleyin</span><span class="sxs-lookup"><span data-stu-id="af576-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="af576-119">"Myiothub" adlı IotHub için hem telemetri hem de operationsmon ""</span><span class="sxs-lookup"><span data-stu-id="af576-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="af576-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af576-120">PARAMETERS</span></span>

### <span data-ttu-id="af576-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="af576-121">-CloudToDevice</span></span>
<span data-ttu-id="af576-122">Cihaza bulut için komut sırası özellikleri.</span><span class="sxs-lookup"><span data-stu-id="af576-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-123">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="af576-123">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="af576-124">Dosyanın karşıya yüklenmesi için bildirimlerin etkinleştirilip etkinleştirilmeyeceğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="af576-124">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-125">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="af576-125">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="af576-126">Gün içinde bekletme süresi.</span><span class="sxs-lookup"><span data-stu-id="af576-126">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-127">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="af576-127">-FallbackRoute</span></span>
<span data-ttu-id="af576-128">Yönlendirme için geri dönüş rotası</span><span class="sxs-lookup"><span data-stu-id="af576-128">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-129">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="af576-129">-FileUploadContainerName</span></span>
<span data-ttu-id="af576-130">Dosyaların yükleneceği kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="af576-130">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-131">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="af576-131">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="af576-132">Karşıya yükleme bildirimlerinin en yüksek teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="af576-132">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-133">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="af576-133">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="af576-134">Dosya karşıya yükleme bildirim sırasındaki iletilerin yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="af576-134">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-135">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="af576-135">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="af576-136">Dosya karşıya yükleme için oluşturulan SAS URI 'Si için yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="af576-136">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-137">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="af576-137">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="af576-138">Dosyaların karşıya yükleneceği depolama bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="af576-138">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="af576-139">-Name</span></span>
<span data-ttu-id="af576-140">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="af576-140">Name of the IotHub</span></span>

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

### <span data-ttu-id="af576-141">-Operationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="af576-141">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="af576-142">İşlem izleme ile ilgili özellikler.</span><span class="sxs-lookup"><span data-stu-id="af576-142">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af576-143">-ResourceGroupName</span></span>
<span data-ttu-id="af576-144">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="af576-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af576-145">-Rotalar</span><span class="sxs-lookup"><span data-stu-id="af576-145">-Routes</span></span>
<span data-ttu-id="af576-146">Yönlendirme için eklenecek yollar</span><span class="sxs-lookup"><span data-stu-id="af576-146">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-147">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="af576-147">-RoutingProperties</span></span>
<span data-ttu-id="af576-148">İletileri dış uç noktalara yönlendirmek için yönlendirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="af576-148">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-149">-SkuName</span><span class="sxs-lookup"><span data-stu-id="af576-149">-SkuName</span></span>
<span data-ttu-id="af576-150">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="af576-150">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-151">-Birimler</span><span class="sxs-lookup"><span data-stu-id="af576-151">-Units</span></span>
<span data-ttu-id="af576-152">Birim sayısı</span><span class="sxs-lookup"><span data-stu-id="af576-152">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="af576-153">-Confirm</span></span>
<span data-ttu-id="af576-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af576-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af576-155">-WhatIf</span></span>
<span data-ttu-id="af576-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af576-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af576-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af576-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af576-158">-DefaultProfile</span></span>
<span data-ttu-id="af576-159">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af576-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af576-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af576-160">CommonParameters</span></span>
<span data-ttu-id="af576-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af576-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af576-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af576-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af576-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af576-163">INPUTS</span></span>

### <span data-ttu-id="af576-164">System. String</span><span class="sxs-lookup"><span data-stu-id="af576-164">System.String</span></span>
<span data-ttu-id="af576-165">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscmontodeviceproperties Microsoft. Azure. Commands. Management. IotHub. modeller. Psoperationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="af576-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="af576-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af576-166">OUTPUTS</span></span>

### <span data-ttu-id="af576-167">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="af576-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="af576-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af576-168">NOTES</span></span>

## <span data-ttu-id="af576-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af576-169">RELATED LINKS</span></span>

