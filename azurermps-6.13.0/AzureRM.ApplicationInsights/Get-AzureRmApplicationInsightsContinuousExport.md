---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: cb5de7f8e0e484c5b9080e3a50871cddca5af173
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591455"
---
# <span data-ttu-id="4cc69-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="4cc69-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="4cc69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc69-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc69-103">Application Insights kaynağı için Application Insights 'ı sürekli dışarı aktarma yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="4cc69-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cc69-104">SYNTAX</span></span>

### <span data-ttu-id="4cc69-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4cc69-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cc69-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="4cc69-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cc69-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4cc69-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc69-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cc69-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc69-109">Application Insights kaynağı için Application Insights 'ı sürekli dışarı aktarma yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="4cc69-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="4cc69-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cc69-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc69-111">Örnek 1 Application Insights kaynağı için sürekli dışarı aktarma alma</span><span class="sxs-lookup"><span data-stu-id="4cc69-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="4cc69-112">"Testgroup" kaynak grubundaki "test" adlı kaynak için Application Insights sürekli dışarı aktarma yapılandırmalarını edinin</span><span class="sxs-lookup"><span data-stu-id="4cc69-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="4cc69-113">Örnek 2 bir Application Insights kaynağı için sürekli dışarı aktarma alma</span><span class="sxs-lookup"><span data-stu-id="4cc69-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="4cc69-114">"Testgroup" kaynak grubundaki "test" adlı kaynak için "ZJrfffySPdtG3ESn3iRxVIEFuNY</span><span class="sxs-lookup"><span data-stu-id="4cc69-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="4cc69-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cc69-115">PARAMETERS</span></span>

### <span data-ttu-id="4cc69-116">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="4cc69-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4cc69-117">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4cc69-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4cc69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc69-118">-DefaultProfile</span></span>
<span data-ttu-id="4cc69-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cc69-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc69-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="4cc69-120">-ExportId</span></span>
<span data-ttu-id="4cc69-121">Application Insights sürekli dışarı aktarma kimliği.</span><span class="sxs-lookup"><span data-stu-id="4cc69-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="4cc69-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cc69-122">-Name</span></span>
<span data-ttu-id="4cc69-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="4cc69-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="4cc69-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc69-124">-ResourceGroupName</span></span>
<span data-ttu-id="4cc69-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4cc69-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4cc69-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4cc69-126">-ResourceId</span></span>
<span data-ttu-id="4cc69-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4cc69-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4cc69-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc69-128">CommonParameters</span></span>
<span data-ttu-id="4cc69-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cc69-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc69-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc69-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc69-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cc69-131">INPUTS</span></span>

### <span data-ttu-id="4cc69-132">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4cc69-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="4cc69-133">Parametreler: Applicationınsightscomponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4cc69-133">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="4cc69-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc69-134">System.String</span></span>

## <span data-ttu-id="4cc69-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cc69-135">OUTPUTS</span></span>

### <span data-ttu-id="4cc69-136">Microsoft. Azure. Commands. ApplicationInsights. model. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cc69-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="4cc69-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cc69-137">NOTES</span></span>

## <span data-ttu-id="4cc69-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cc69-138">RELATED LINKS</span></span>
