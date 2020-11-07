---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: f30d5da085658c979a52f166469e4e548afdaf7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917635"
---
# <span data-ttu-id="0ff89-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="0ff89-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="0ff89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff89-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff89-103">Yeni bir Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ff89-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="0ff89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ff89-104">SYNTAX</span></span>

### <span data-ttu-id="0ff89-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ff89-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff89-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="0ff89-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff89-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0ff89-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff89-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ff89-108">DESCRIPTION</span></span>
<span data-ttu-id="0ff89-109">Yeni bir Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ff89-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="0ff89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ff89-110">EXAMPLES</span></span>

### <span data-ttu-id="0ff89-111">Örnek 1 Application Insights kaynağı için yeni bir sürekli dışarı aktarma yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ff89-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="0ff89-112">Yeni Application Insights sürekli dışarı aktarma yapılandırması "Istek" ve "Izleme" belge türlerini depolama alanına "testgroup" kaynak grubundaki "teststorageaccount" depolama hesabında "testcontainer" içerir.</span><span class="sxs-lookup"><span data-stu-id="0ff89-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="0ff89-113">SAS belirtecinin geçerli olması ve kapsayıcıya yazma izni olması gerekir, aksi takdirde dışarı aktarma özelliği çalışmaz. SAS belirtecinin süresi dolduysa, sürekli dışarı aktarma özelliği çalışmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="0ff89-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="0ff89-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ff89-114">PARAMETERS</span></span>

### <span data-ttu-id="0ff89-115">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="0ff89-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0ff89-116">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0ff89-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0ff89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff89-117">-DefaultProfile</span></span>
<span data-ttu-id="0ff89-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ff89-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff89-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="0ff89-119">-DocumentType</span></span>
<span data-ttu-id="0ff89-120">Dışarı aktarılan belge türleri.</span><span class="sxs-lookup"><span data-stu-id="0ff89-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="0ff89-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ff89-121">-Name</span></span>
<span data-ttu-id="0ff89-122">Bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="0ff89-122">Component Name.</span></span>

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

### <span data-ttu-id="0ff89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff89-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ff89-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0ff89-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="0ff89-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0ff89-125">-ResourceId</span></span>
<span data-ttu-id="0ff89-126">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0ff89-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0ff89-127">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="0ff89-127">-StorageAccountId</span></span>
<span data-ttu-id="0ff89-128">Hedef depolama hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="0ff89-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="0ff89-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="0ff89-129">-StorageLocation</span></span>
<span data-ttu-id="0ff89-130">Hedef depolama konumu kimliği.</span><span class="sxs-lookup"><span data-stu-id="0ff89-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="0ff89-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="0ff89-131">-StorageSASUri</span></span>
<span data-ttu-id="0ff89-132">Hedef depolama SAS Uri 'Si.</span><span class="sxs-lookup"><span data-stu-id="0ff89-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="0ff89-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ff89-133">-Confirm</span></span>
<span data-ttu-id="0ff89-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ff89-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff89-135">-WhatIf</span></span>
<span data-ttu-id="0ff89-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ff89-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ff89-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ff89-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff89-138">CommonParameters</span></span>
<span data-ttu-id="0ff89-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ff89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff89-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff89-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff89-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ff89-141">INPUTS</span></span>

### <span data-ttu-id="0ff89-142">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0ff89-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0ff89-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff89-143">System.String</span></span>

## <span data-ttu-id="0ff89-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ff89-144">OUTPUTS</span></span>

### <span data-ttu-id="0ff89-145">Microsoft. Azure. Commands. ApplicationInsights. model. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ff89-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="0ff89-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ff89-146">NOTES</span></span>

## <span data-ttu-id="0ff89-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ff89-147">RELATED LINKS</span></span>
