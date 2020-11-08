---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279716"
---
# <span data-ttu-id="df007-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="df007-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="df007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df007-102">SYNOPSIS</span></span>
<span data-ttu-id="df007-103">Application Insights kaynağında sürekli dışarı aktarma yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="df007-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="df007-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df007-104">SYNTAX</span></span>

### <span data-ttu-id="df007-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df007-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df007-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="df007-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df007-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="df007-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df007-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="df007-108">DESCRIPTION</span></span>
<span data-ttu-id="df007-109">Application Insights kaynağında sürekli dışarı aktarma yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="df007-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="df007-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df007-110">EXAMPLES</span></span>

### <span data-ttu-id="df007-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df007-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="df007-112">"Testgroup" kaynak grubundaki "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" kaynak grubundaki sürekli dışarı aktarma yapılandırmasını "=" kaynak grubunda "teststorageaccount" içinde "testcontainer" depolama kapsayıcısına aktarmak için güncelleştirin. SAS belirtecinin geçerli olması ve kapsayıcıya yazma izni olması gerekir, aksi takdirde sürekli dışarı aktarma özelliği çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df007-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="df007-113">SAS belirtecinin süresi dolduysa, sürekli dışarı aktarma özelliği çalışmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="df007-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="df007-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df007-114">PARAMETERS</span></span>

### <span data-ttu-id="df007-115">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="df007-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="df007-116">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="df007-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df007-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df007-117">-DefaultProfile</span></span>
<span data-ttu-id="df007-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df007-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df007-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="df007-119">-DisableConfiguration</span></span>
<span data-ttu-id="df007-120">Sürekli dışarı aktarmayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="df007-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="df007-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="df007-121">-DocumentType</span></span>
<span data-ttu-id="df007-122">Dışarı aktarılan belge türleri.</span><span class="sxs-lookup"><span data-stu-id="df007-122">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="df007-123">-ExportId</span></span>
<span data-ttu-id="df007-124">Application Insights sürekli dışarı aktarma kimliği.</span><span class="sxs-lookup"><span data-stu-id="df007-124">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="df007-125">-Name</span></span>
<span data-ttu-id="df007-126">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="df007-126">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df007-127">-ResourceGroupName</span></span>
<span data-ttu-id="df007-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="df007-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="df007-129">-ResourceId</span></span>
<span data-ttu-id="df007-130">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="df007-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df007-131">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="df007-131">-StorageAccountId</span></span>
<span data-ttu-id="df007-132">Hedef depolama hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="df007-132">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="df007-133">-StorageLocation</span></span>
<span data-ttu-id="df007-134">Hedef depolama konumu kimliği.</span><span class="sxs-lookup"><span data-stu-id="df007-134">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="df007-135">-StorageSASUri</span></span>
<span data-ttu-id="df007-136">Hedef depolama SAS Uri 'si.</span><span class="sxs-lookup"><span data-stu-id="df007-136">Destination Storage SAS uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df007-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="df007-137">-Confirm</span></span>
<span data-ttu-id="df007-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df007-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df007-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df007-139">-WhatIf</span></span>
<span data-ttu-id="df007-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df007-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df007-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df007-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df007-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df007-142">CommonParameters</span></span>
<span data-ttu-id="df007-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df007-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df007-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df007-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df007-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df007-145">INPUTS</span></span>

### <span data-ttu-id="df007-146">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="df007-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="df007-147">System. String</span><span class="sxs-lookup"><span data-stu-id="df007-147">System.String</span></span>

## <span data-ttu-id="df007-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df007-148">OUTPUTS</span></span>

### <span data-ttu-id="df007-149">Microsoft. Azure. Commands. ApplicationInsights. model. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="df007-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="df007-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df007-150">NOTES</span></span>

## <span data-ttu-id="df007-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df007-151">RELATED LINKS</span></span>
