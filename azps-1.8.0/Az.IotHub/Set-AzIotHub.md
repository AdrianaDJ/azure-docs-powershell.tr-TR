---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: ca7fe171e95d87dd054f0dac27e1a5ccd07396a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916404"
---
# <span data-ttu-id="2afe8-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="2afe8-101">Set-AzIotHub</span></span>

## <span data-ttu-id="2afe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2afe8-102">SYNOPSIS</span></span>
<span data-ttu-id="2afe8-103">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2afe8-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="2afe8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2afe8-104">SYNTAX</span></span>

### <span data-ttu-id="2afe8-105">UpdateSku (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2afe8-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-109">Updateoperationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-110">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-111">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe8-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="2afe8-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2afe8-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="2afe8-113">DESCRIPTION</span></span>
<span data-ttu-id="2afe8-114">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2afe8-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="2afe8-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2afe8-115">EXAMPLES</span></span>

### <span data-ttu-id="2afe8-116">Örnek 1 STB 'yi güncelleyin</span><span class="sxs-lookup"><span data-stu-id="2afe8-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="2afe8-117">"Myiothub" adlı IotHub için STB 'yi S1 ve birimler 'i 5 olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2afe8-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2afe8-118">Örnek 2 eventhub özelliklerini güncelleyin</span><span class="sxs-lookup"><span data-stu-id="2afe8-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="2afe8-119">"Myiothub" adlı IotHub için hem telemetri hem de operationsmon ""</span><span class="sxs-lookup"><span data-stu-id="2afe8-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2afe8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2afe8-120">PARAMETERS</span></span>

### <span data-ttu-id="2afe8-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="2afe8-121">-CloudToDevice</span></span>
<span data-ttu-id="2afe8-122">Cihaza bulut için komut sırası özellikleri.</span><span class="sxs-lookup"><span data-stu-id="2afe8-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="2afe8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afe8-123">-DefaultProfile</span></span>
<span data-ttu-id="2afe8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2afe8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2afe8-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="2afe8-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="2afe8-126">Dosyanın karşıya yüklenmesi için bildirimlerin etkinleştirilip etkinleştirilmeyeceğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="2afe8-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="2afe8-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="2afe8-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="2afe8-128">Gün içinde bekletme süresi.</span><span class="sxs-lookup"><span data-stu-id="2afe8-128">Retention time in days.</span></span> 

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

### <span data-ttu-id="2afe8-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="2afe8-129">-FallbackRoute</span></span>
<span data-ttu-id="2afe8-130">Yönlendirme için geri dönüş rotası</span><span class="sxs-lookup"><span data-stu-id="2afe8-130">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="2afe8-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="2afe8-131">-FileUploadContainerName</span></span>
<span data-ttu-id="2afe8-132">Dosyaların yükleneceği kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="2afe8-132">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="2afe8-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="2afe8-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="2afe8-134">Karşıya yükleme bildirimlerinin en yüksek teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="2afe8-134">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="2afe8-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="2afe8-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="2afe8-136">Dosya karşıya yükleme bildirim sırasındaki iletilerin yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="2afe8-136">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="2afe8-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="2afe8-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="2afe8-138">Dosya karşıya yükleme için oluşturulan SAS URI 'Si için yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="2afe8-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="2afe8-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="2afe8-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="2afe8-140">Dosyaların karşıya yükleneceği depolama bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="2afe8-140">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="2afe8-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="2afe8-141">-Name</span></span>
<span data-ttu-id="2afe8-142">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="2afe8-142">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe8-143">-Operationsmenıtoringproperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="2afe8-144">İşlem izleme ile ilgili özellikler.</span><span class="sxs-lookup"><span data-stu-id="2afe8-144">The properties related to operations monitoring.</span></span> 

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

### <span data-ttu-id="2afe8-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2afe8-145">-ResourceGroupName</span></span>
<span data-ttu-id="2afe8-146">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2afe8-146">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe8-147">-Rotalar</span><span class="sxs-lookup"><span data-stu-id="2afe8-147">-Routes</span></span>
<span data-ttu-id="2afe8-148">Yönlendirme için eklenecek yollar</span><span class="sxs-lookup"><span data-stu-id="2afe8-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="2afe8-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="2afe8-149">-RoutingProperties</span></span>
<span data-ttu-id="2afe8-150">İletileri dış uç noktalara yönlendirmek için yönlendirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="2afe8-150">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="2afe8-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2afe8-151">-SkuName</span></span>
<span data-ttu-id="2afe8-152">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="2afe8-152">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2afe8-153">-Birimler</span><span class="sxs-lookup"><span data-stu-id="2afe8-153">-Units</span></span>
<span data-ttu-id="2afe8-154">Birim sayısı</span><span class="sxs-lookup"><span data-stu-id="2afe8-154">Number of Units</span></span>

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

### <span data-ttu-id="2afe8-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="2afe8-155">-Confirm</span></span>
<span data-ttu-id="2afe8-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2afe8-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2afe8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2afe8-157">-WhatIf</span></span>
<span data-ttu-id="2afe8-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2afe8-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2afe8-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2afe8-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2afe8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afe8-160">CommonParameters</span></span>
<span data-ttu-id="2afe8-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2afe8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afe8-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afe8-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afe8-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2afe8-163">INPUTS</span></span>

### <span data-ttu-id="2afe8-164">System. String</span><span class="sxs-lookup"><span data-stu-id="2afe8-164">System.String</span></span>

## <span data-ttu-id="2afe8-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2afe8-165">OUTPUTS</span></span>

### <span data-ttu-id="2afe8-166">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="2afe8-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="2afe8-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2afe8-167">NOTES</span></span>

## <span data-ttu-id="2afe8-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2afe8-168">RELATED LINKS</span></span>