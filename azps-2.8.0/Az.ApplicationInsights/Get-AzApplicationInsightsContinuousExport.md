---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: e6e1e2319ade47557ddf07f34a9371a4bbd532b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753381"
---
# <span data-ttu-id="95562-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="95562-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="95562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95562-102">SYNOPSIS</span></span>
<span data-ttu-id="95562-103">Application Insights kaynağı için Application Insights 'ı sürekli dışarı aktarma yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="95562-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="95562-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95562-104">SYNTAX</span></span>

### <span data-ttu-id="95562-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95562-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95562-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="95562-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95562-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="95562-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95562-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95562-108">DESCRIPTION</span></span>
<span data-ttu-id="95562-109">Application Insights kaynağı için Application Insights 'ı sürekli dışarı aktarma yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="95562-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="95562-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95562-110">EXAMPLES</span></span>

### <span data-ttu-id="95562-111">Örnek 1 Application Insights kaynağı için sürekli dışarı aktarma alma</span><span class="sxs-lookup"><span data-stu-id="95562-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="95562-112">"Testgroup" kaynak grubundaki "test" adlı kaynak için Application Insights sürekli dışarı aktarma yapılandırmalarını edinin</span><span class="sxs-lookup"><span data-stu-id="95562-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="95562-113">Örnek 2 bir Application Insights kaynağı için sürekli dışarı aktarma alma</span><span class="sxs-lookup"><span data-stu-id="95562-113">Example 2 Get continuous export for an application insights resource</span></span>
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

<span data-ttu-id="95562-114">"Testgroup" kaynak grubundaki "test" adlı kaynak için "ZJrfffySPdtG3ESn3iRxVIEFuNY</span><span class="sxs-lookup"><span data-stu-id="95562-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="95562-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95562-115">PARAMETERS</span></span>

### <span data-ttu-id="95562-116">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="95562-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="95562-117">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="95562-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="95562-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95562-118">-DefaultProfile</span></span>
<span data-ttu-id="95562-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95562-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95562-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="95562-120">-ExportId</span></span>
<span data-ttu-id="95562-121">Application Insights sürekli dışarı aktarma kimliği.</span><span class="sxs-lookup"><span data-stu-id="95562-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="95562-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="95562-122">-Name</span></span>
<span data-ttu-id="95562-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="95562-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="95562-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95562-124">-ResourceGroupName</span></span>
<span data-ttu-id="95562-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="95562-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="95562-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="95562-126">-ResourceId</span></span>
<span data-ttu-id="95562-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="95562-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="95562-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95562-128">CommonParameters</span></span>
<span data-ttu-id="95562-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95562-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95562-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95562-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95562-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95562-131">INPUTS</span></span>

### <span data-ttu-id="95562-132">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="95562-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="95562-133">System. String</span><span class="sxs-lookup"><span data-stu-id="95562-133">System.String</span></span>

## <span data-ttu-id="95562-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95562-134">OUTPUTS</span></span>

### <span data-ttu-id="95562-135">Microsoft. Azure. Commands. ApplicationInsights. model. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="95562-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="95562-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95562-136">NOTES</span></span>

## <span data-ttu-id="95562-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95562-137">RELATED LINKS</span></span>
