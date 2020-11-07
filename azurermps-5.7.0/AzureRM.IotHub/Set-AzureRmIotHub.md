---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765005"
---
# <span data-ttu-id="3cb93-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="3cb93-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="3cb93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb93-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb93-103">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3cb93-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cb93-104">SYNTAX</span></span>

### <span data-ttu-id="3cb93-105">UpdateSku (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3cb93-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-109">Updateoperationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="3cb93-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb93-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cb93-113">DESCRIPTION</span></span>
<span data-ttu-id="3cb93-114">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3cb93-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="3cb93-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cb93-115">EXAMPLES</span></span>

### <span data-ttu-id="3cb93-116">Örnek 1 STB 'yi güncelleyin</span><span class="sxs-lookup"><span data-stu-id="3cb93-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="3cb93-117">"Myiothub" adlı IotHub için STB 'yi S1 ve birimler 'i 5 olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3cb93-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="3cb93-118">Örnek 2 eventhub özelliklerini güncelleyin</span><span class="sxs-lookup"><span data-stu-id="3cb93-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="3cb93-119">"Myiothub" adlı IotHub için hem telemetri hem de operationsmon ""</span><span class="sxs-lookup"><span data-stu-id="3cb93-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="3cb93-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cb93-120">PARAMETERS</span></span>

### <span data-ttu-id="3cb93-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="3cb93-121">-CloudToDevice</span></span>
<span data-ttu-id="3cb93-122">Cihaza bulut için komut sırası özellikleri.</span><span class="sxs-lookup"><span data-stu-id="3cb93-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb93-123">-DefaultProfile</span></span>
<span data-ttu-id="3cb93-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3cb93-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cb93-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="3cb93-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="3cb93-126">Dosyanın karşıya yüklenmesi için bildirimlerin etkinleştirilip etkinleştirilmeyeceğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="3cb93-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="3cb93-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="3cb93-128">Gün içinde bekletme süresi.</span><span class="sxs-lookup"><span data-stu-id="3cb93-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="3cb93-129">-FallbackRoute</span></span>
<span data-ttu-id="3cb93-130">Yönlendirme için geri dönüş rotası</span><span class="sxs-lookup"><span data-stu-id="3cb93-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="3cb93-131">-FileUploadContainerName</span></span>
<span data-ttu-id="3cb93-132">Dosyaların yükleneceği kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="3cb93-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3cb93-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="3cb93-134">Karşıya yükleme bildirimlerinin en yüksek teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="3cb93-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="3cb93-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="3cb93-136">Dosya karşıya yükleme bildirim sırasındaki iletilerin yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="3cb93-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="3cb93-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="3cb93-138">Dosya karşıya yükleme için oluşturulan SAS URI 'Si için yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="3cb93-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="3cb93-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="3cb93-140">Dosyaların karşıya yükleneceği depolama bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="3cb93-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cb93-141">-Name</span></span>
<span data-ttu-id="3cb93-142">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="3cb93-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-143">-Operationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="3cb93-144">İşlem izleme ile ilgili özellikler.</span><span class="sxs-lookup"><span data-stu-id="3cb93-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb93-145">-ResourceGroupName</span></span>
<span data-ttu-id="3cb93-146">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3cb93-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-147">-Rotalar</span><span class="sxs-lookup"><span data-stu-id="3cb93-147">-Routes</span></span>
<span data-ttu-id="3cb93-148">Yönlendirme için eklenecek yollar</span><span class="sxs-lookup"><span data-stu-id="3cb93-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="3cb93-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-149">-RoutingProperties</span></span>
<span data-ttu-id="3cb93-150">İletileri dış uç noktalara yönlendirmek için yönlendirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="3cb93-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3cb93-151">-SkuName</span></span>
<span data-ttu-id="3cb93-152">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="3cb93-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-153">-Birimler</span><span class="sxs-lookup"><span data-stu-id="3cb93-153">-Units</span></span>
<span data-ttu-id="3cb93-154">Birim sayısı</span><span class="sxs-lookup"><span data-stu-id="3cb93-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cb93-155">-Confirm</span></span>
<span data-ttu-id="3cb93-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cb93-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb93-157">-WhatIf</span></span>
<span data-ttu-id="3cb93-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cb93-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb93-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cb93-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb93-160">CommonParameters</span></span>
<span data-ttu-id="3cb93-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cb93-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb93-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb93-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb93-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cb93-163">INPUTS</span></span>

### <span data-ttu-id="3cb93-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3cb93-164">System.String</span></span>
<span data-ttu-id="3cb93-165">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscmontodeviceproperties Microsoft. Azure. Commands. Management. IotHub. modeller. Psoperationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="3cb93-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="3cb93-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cb93-166">OUTPUTS</span></span>

### <span data-ttu-id="3cb93-167">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="3cb93-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="3cb93-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cb93-168">NOTES</span></span>

## <span data-ttu-id="3cb93-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cb93-169">RELATED LINKS</span></span>

