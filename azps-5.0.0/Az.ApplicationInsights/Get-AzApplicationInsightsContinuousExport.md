---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: d5711e6bca9b0579b456e4d2b0c5f915b4ad6fe0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322705"
---
# <span data-ttu-id="553dc-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="553dc-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="553dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="553dc-102">SYNOPSIS</span></span>
<span data-ttu-id="553dc-103">Application Insights kaynağı için Application Insights 'ı sürekli dışarı aktarma yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="553dc-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="553dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="553dc-104">SYNTAX</span></span>

### <span data-ttu-id="553dc-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="553dc-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="553dc-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="553dc-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="553dc-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="553dc-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="553dc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="553dc-108">DESCRIPTION</span></span>
<span data-ttu-id="553dc-109">Application Insights kaynağı için Application Insights 'ı sürekli dışarı aktarma yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="553dc-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="553dc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="553dc-110">EXAMPLES</span></span>

### <span data-ttu-id="553dc-111">Örnek 1 Application Insights kaynağı için sürekli dışarı aktarma alma</span><span class="sxs-lookup"><span data-stu-id="553dc-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="553dc-112">"Testgroup" kaynak grubundaki "test" adlı kaynak için Application Insights sürekli dışarı aktarma yapılandırmalarını edinin</span><span class="sxs-lookup"><span data-stu-id="553dc-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="553dc-113">Örnek 2 bir Application Insights kaynağı için sürekli dışarı aktarma alma</span><span class="sxs-lookup"><span data-stu-id="553dc-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="553dc-114">"Testgroup" kaynak grubundaki "test" adlı kaynak için "ZJrfffySPdtG3ESn3iRxVIEFuNY</span><span class="sxs-lookup"><span data-stu-id="553dc-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="553dc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="553dc-115">PARAMETERS</span></span>

### <span data-ttu-id="553dc-116">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="553dc-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="553dc-117">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="553dc-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="553dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553dc-118">-DefaultProfile</span></span>
<span data-ttu-id="553dc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="553dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="553dc-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="553dc-120">-ExportId</span></span>
<span data-ttu-id="553dc-121">Application Insights sürekli dışarı aktarma kimliği.</span><span class="sxs-lookup"><span data-stu-id="553dc-121">Application Insights Continuous Export Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553dc-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="553dc-122">-Name</span></span>
<span data-ttu-id="553dc-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="553dc-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="553dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="553dc-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="553dc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="553dc-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="553dc-126">-ResourceId</span></span>
<span data-ttu-id="553dc-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="553dc-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="553dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553dc-128">CommonParameters</span></span>
<span data-ttu-id="553dc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="553dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553dc-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553dc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553dc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="553dc-131">INPUTS</span></span>

### <span data-ttu-id="553dc-132">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="553dc-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="553dc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="553dc-133">System.String</span></span>

## <span data-ttu-id="553dc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="553dc-134">OUTPUTS</span></span>

### <span data-ttu-id="553dc-135">Microsoft. Azure. Commands. ApplicationInsights. model. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="553dc-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="553dc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="553dc-136">NOTES</span></span>

## <span data-ttu-id="553dc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="553dc-137">RELATED LINKS</span></span>
